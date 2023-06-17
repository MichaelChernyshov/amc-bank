<script setup>
import WelcomeComp from '../components/main/WelcomeComp.vue'
import GuidesMain from '../components/GuidesMain.vue';
</script>

<template>
  <main>
    <WelcomeComp></WelcomeComp>
    <v-divider class="divider"></v-divider>
    <GuidesMain 
    pageTitle="Using guide" 
    fCardTitle="Instalation" 
    fCardDescription="You can download our app on your device" 
    fImgLink="./public/images/icons/iphone-icon.svg" 
    sCardTitle="Registration" 
    sCardDescription="Fill all forms to end registration" 
    sImgLink="./public/images/icons/folderGuide.svg" 
    tCardTitle="Using" 
    tCardDescription="Now you can start using you cards in app of our bank" 
    tImgLink="./public/images/icons/CardsGuide.svg"></GuidesMain>
  </main>
</template>

<style lang="scss">
.divider {
  margin: 0 0 5%;
}
</style>