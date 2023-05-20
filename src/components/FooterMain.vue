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
    <v-footer class="d-flex flex-column">
      <div class="d-flex w-100 px-4">
        <div class="px-4 py-2 w-100 footer-text">
        {{ new Date().getFullYear() }} AMC - Bank
        </div>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4"
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
    padding: 0 !important;
    background: none !important;
}
.footer-text {
    font-size: 13px;
    color: #BDBDBD;
}
</style>