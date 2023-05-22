<script>
    // export default {
    //     data () {
    //   return {
    //     show1: false,
    //     show2: true,
    //     password: 'Password',
    //     rules: {
    //       required: value => !!value || 'Required.',
    //       min: v => v.length >= 8 || 'Min 8 characters',
    //       emailMatch: () => (`The email and password you entered don't match`),
    //     },
    //   }
    // },
    // }

    export default {
    data: () => ({
      show1: false,
      show2: true,
      form: false,
      email: null,
      password: null,
      loading: false,
    }),

    methods: {
      onSubmit () {
        if (!this.form) return

        this.loading = true

        setTimeout(() => (
            this.loading = false,
            alert("You have logined successfully")
            ), 2000)
      },
      required (v) {
        return !!v || 'Field is required'
      },
    },
  }
</script>
<template>
    <!-- <div class="d-flex align-center justify-center" style="height: 70vh">
        <v-sheet class="mx-auto" theme="dark">
            <v-form fast-fail @submit.prevent="login">
                <v-text-field  variant="underlined" v-model="username" label="User Name"></v-text-field>

                <v-text-field 
                variant="underlined" 
                v-model="password" 
                label="password"
                :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
                :rules="[rules.required, rules.min]"
                :type="show1 ? 'text' : 'password'"
                hint="At least 8 characters"
                counter
                @click:append="show1 = !show1"
                >
                </v-text-field>
                <a href="#" class="text-body-2 font-weight-regular">Forgot Password?</a>

                <v-btn type="submit" variant="outlined" color="primary" block class="mt-2">Sign in</v-btn>

            </v-form>
            <div class="mt-2">
                <p class="text-body-2">Don't have an account? <a href="#">Sign Up</a></p>
            </div>
        </v-sheet>
    </div> -->
<div class="login d-flex align-center justify-center">
    <h1 class="bank-welcome">We welcome you to your online bank account</h1>
  <v-sheet class="pa-12" rounded>
    <v-card class="mx-auto px-6 py-8">
      <v-form
        v-model="form"
        @submit.prevent="onSubmit"
      >
        <v-text-field
          v-model="email"
          :readonly="loading"
          :rules="[required]"
          class="mb-2"
          label="Email"
          placeholder="Enter your email"
          variant="outlined"
        ></v-text-field>

        <v-text-field
          v-model="password"
          :readonly="loading"
          :rules="[required]"
          :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
          :type="show1 ? 'text' : 'password'"
          label="Password"
          placeholder="Enter your password"
          variant="outlined"
          @click:append="show1 = !show1"
        ></v-text-field>

        <br>

        <v-btn
          :disabled="!form"
          :loading="loading"
          block
          color="success"
          size="large"
          type="submit"
          variant="elevated"
        >
          Sign In
        </v-btn>
      </v-form>
    </v-card>
  </v-sheet>
</div>
</template>

<style lang="scss">
.bank-welcome {
    font-size: 3rem;
    width: 30%;
}
.v-sheet {
    background: none;
    width: 40%;
}
.login {
    height: 70vh;
}

.bg-success {
    background-color: rgb(26, 31, 183) !important;
}
.v-btn--disabled.v-btn--variant-elevated .v-btn__overlay, .v-btn--disabled.v-btn--variant-flat .v-btn__overlay {
    opacity: 0;
}
</style>