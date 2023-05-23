<script setup>
import NavBar from './components/header/NavBar.vue'
import FooterMain from './components/footer/FooterMain.vue';
</script>

<template>
  <v-app>
    <NavBar />
    <v-main>
      <RouterView />
    </v-main>
    <FooterMain />
  </v-app>
  </template>