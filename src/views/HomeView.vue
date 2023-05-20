<script setup>
import WelcomeComp from '../components/WelcomeComp.vue'
import WelcomeGuide from '../components/WelcomeGuide.vue';
</script>

<template>
  <main>
    <WelcomeComp></WelcomeComp>
    <v-divider class="ma-9"></v-divider>
    <WelcomeGuide fCardTitle="Instalation" fCardDescription="You can download our app on your device" imgLink="/src/assets/images/icons/iphone-icon.svg"></WelcomeGuide>
  </main>
</template>