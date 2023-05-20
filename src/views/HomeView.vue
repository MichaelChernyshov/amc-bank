<script setup>
import WelcomeComp from '../components/WelcomeComp.vue'
import GuidesMain from '../components/GuidesMain.vue';
</script>

<template>
  <main>
    <WelcomeComp></WelcomeComp>
    <v-divider class="ma-9"></v-divider>
    <GuidesMain pageTitle="Using guide" fCardTitle="Instalation" fCardDescription="You can download our app on your device" fImgLink="/src/assets/images/icons/iphone-icon.svg" sCardTitle="Registration" sCardDescription="Fill all forms to end registration" sImgLink="/src/assets/images/icons/folderGuide.svg" tCardTitle="Using" tCardDescription="Now you can start using you cards in app of our bank" tImgLink="/src/assets/images/icons/CardsGuide.svg"></GuidesMain>
  </main>
</template>