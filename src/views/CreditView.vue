<script setup>
import CardsTitle from '../components/CardsTitle.vue';
// import CardsButtons from '../components/CardsButtons.vue'
import CardDescription from '../components/CardDescription.vue';
import OrderFormCredit from '../components/OrderFormCredit.vue';
</script>

<template>
  <CardsTitle cardType="Credit" cardDescription="Allows you to pay for purchases at the expense of the bank. Pay with a card and get cashback for any purchases"></CardsTitle>
  <!-- <CardsButtons cardName="4U Credit" cardType="Credit"></CardsButtons> -->
  <CardDescription cardName="Aurora" description="Using credit card you can buy whatever you want with special offers" imgLink="/src/assets/images/cards/CardCredit.svg"></CardDescription>
  <OrderFormCredit></OrderFormCredit>
</template>