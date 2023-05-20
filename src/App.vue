<script setup>
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
import FooterMain from './components/FooterMain.vue'
</script>

<template>
  <NavBar />
  <RouterView />
  <FooterMain />
</template>
