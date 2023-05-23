<script>
export default {
    data: () => ({
      drawer: false,
      group: null,
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
  }
</script>

<template> 
    <v-toolbar app color="transparent px-9 py-5">
      <v-toolbar-title>
        <div class="nav-logo ">
                <a href="/">
                    <div class="logo"></div>
                </a>
        </div>
      </v-toolbar-title>

        <v-spacer></v-spacer>

        <nav class="nav_bar__link hidden-sm-and-down">
          <v-btn variant="plain" :ripple="false" to="/debit" class="text-capitalize transition rounded-xl">Debit Card</v-btn>
          <v-btn variant="plain" :ripple="false" to="/credit" class="text-capitalize transition rounded-xl">Credit Card</v-btn>
          <v-btn variant="plain" :ripple="false" to="/deposit" class="text-capitalize transition rounded-xl">Deposit</v-btn>
          <v-btn variant="plain" :ripple="false" to="/e-sim" class="text-capitalize transition rounded-xl">eSIM</v-btn>
          <v-btn variant="outlined" :ripple="false" to="/login" class="text-capitalize transition entr-btn entr-border">Enter</v-btn>
        </nav> 
      <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer" class="hidden-md-and-up"></v-app-bar-nav-icon>
    </v-toolbar>
 
    <v-navigation-drawer
      app
      v-model="drawer"
      location="right"
      temporary
      color="white"
    >
      <v-list>
        <v-list-item>
          <RouterLink to="/debit" class="transition">Debit Card</RouterLink>
        </v-list-item>

        <v-list-item>
          <RouterLink to="/credit" class="transition">Credit Card</RouterLink>
        </v-list-item>

        <v-list-item>
          <RouterLink to="/deposit" class="transition">Deposit</RouterLink>
        </v-list-item>

        <v-list-item>
          <RouterLink to="/e-sim" class="transition">eSIM</RouterLink>
        </v-list-item>

        <v-list-item>
          <RouterLink to="/login" class="btn-enter transition">Enter</RouterLink>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
</template>

<style lang="scss">
.entr-btn.entr-border {
    border: 3px solid rgb(12, 24, 81);
    border-radius: 28px;

     &:hover {
            border: 2px solid rgb(25, 48, 164);
        }
}
   .nav-logo {

        .logo {
            background: no-repeat url(/src/assets/images/logo/logoWhite.svg);
            width: 6rem;
            height: 3rem;
            
            @include large {
                width: 9rem;
                height: 4rem;
            }
            @include medium {
                width: 7rem;
                height: 3rem;
            }
            @include small {
                width: 6rem;
                height: 2.5rem;
            }
        } 
    }
.v-app-bar.v-toolbar:not(.v-toolbar--flat) {
    box-shadow: unset !important;
}
.v-card {
    padding: 0 !important;
}
.nav_bar__link {
    a {
        margin-left: 2rem;
        transition: transform .4s cubic-bezier(0,0,.4,1);

        @include large {
            margin-left: 3rem ;
        }

        &:hover {
            color: white;
            transform: scale3d(1.15,1.15,1.15);
        }

        &:first-child {
            margin-left: 0;
        }
    }
}
.v-application {
  background: radial-gradient(100% 100% at -22% -14%, #1D38C2FF 0%, #FF000000 85%),radial-gradient(100% 100% at 116% 118%, #1D38C2FF 0%, #FF000000 85%),linear-gradient(0deg, #1E1E20FF 0%, #111010FF 94%) !important;
  color: white !important;
  display: block !important;
}

.v-card--variant-elevated, .v-card--variant-flat {
  background: rgba(21, 74, 207, 0) !important;
}
</style>
