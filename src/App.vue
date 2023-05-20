<script setup>
import { RouterView } from 'vue-router'
import NavBar from './components/header/NavBar.vue'
import FooterMain from './components/footer/FooterMain.vue'
</script>

<template>
  <v-app>
    <NavBar />
    <RouterView />
    <FooterMain />
  </v-app>
</template>

<style lang="scss">
.v-application {
  background: radial-gradient(100% 100% at -22% -14%, #1D38C2FF 0%, #FF000000 85%),radial-gradient(100% 100% at 116% 118%, #1D38C2FF 0%, #FF000000 85%),linear-gradient(0deg, #1E1E20FF 0%, #111010FF 94%) !important;
  color: white !important;
  display: block !important;
}</style>