<script>
  export default {
    data: () => ({
      icons: [
        'mdi-facebook',
        'mdi-twitter',
        'mdi-instagram',
      ],
    }),
  }
</script>

<template>
    <v-footer class="d-flex">
      <div class="d-flex w-100 px-4 align-center">
        <div class="px-4 py-2 w-100 footer-text">
        {{ new Date().getFullYear() }} AMC - Bank
        </div>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 buttons"
          :icon="icon"
          variant="plain"
          size="x-small"
        ></v-btn>
      </div>
    </v-footer>
  </template>

<style lang="scss">
.v-footer {
    color: white !important;
    padding: 5% 0 0 !important;
    background: none !important;
}
.footer-text {
    font-size: 10px;
    color: #BDBDBD;
    @include large {
        font-size: 1.5rem;    
    }
    @include medium {
        font-size: 1.2rem;    
    }
    @include small {
        font-size: 1rem;    
    }
    @include extra-small {
        font-size: 0.6rem;    
    }
}

.v-icon--size-default {
  font-size: 0.7rem; 

  @include large {
        font-size: 1.8rem !important;    
    }
    @include medium {
        font-size: 1.5rem !important;    
    }
    @include small {
        font-size: 1.5rem !important;    
    }
    @include extra-small {
        font-size: 1rem !important;    
    }
}
</style>