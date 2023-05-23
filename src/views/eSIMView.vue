<script setup>
import ESim from '../components/e-sim/ESim.vue';
import ESimDescription from '../components/e-sim/ESimDescription.vue'
import ESimInstall from '../components/e-sim/ESimInstall.vue'
import ESimCompatible from '../components/e-sim/ESimCompatible.vue'
import QuestionsPanel from '../components/e-sim/QuestionsPanel.vue'
</script>

<template>
    <ESim />
    <ESimDescription />
    <ESimInstall />
    <ESimCompatible />
    <QuestionsPanel titleF="Can the eSIM be moved to another device?" 
    textF="Yes. If you have removed the eSIM from your device, you can download it to another device. For this
use the same QR code. You can use it up to 100 times. Be sure to make sure when removing the eSIM that there is an Internet connection through the physical SIM card
or Wi-Fi, otherwise the command to remove the eSIM from the device will not be sent, and the card will not actually be removed."
    titleS="Do I need to save the QR code?"
    textS="Yes. You may need it for re-installation if you decide to rearrange the eSIM. The QR code is an access to your number, keep it in a safe place."
    titleT="What to do if the QR code is lost?"
    textT="If before that you did not read the QR code or read it, but then deleted the eSIM, contact AMC. Employees will help you replace the eSIM with a new one."
    />
  </template>

<style lang="scss">
</style>