<script setup>
import CardsTitle from '../components/CardsTitle.vue';
import CardDescription from '../components/CardDescription.vue';
import OrderFormDebit from '../components/OrderFormDebit.vue';
// import CardsButtons from '../components/CardsButtons.vue'
</script>

<template>
    <CardsTitle cardType="Debit" cardDescription="Using debit card is the best way to pay for everything you want and after all - receive a cashback"></CardsTitle>
    <!-- <CardsButtons cardName="4U Debit" cardType="Debit"></CardsButtons> -->
    <CardDescription cardName="Galaxy" description="Debit card that you can use everywhere you want and take all advantages of it without any problems" imgLink="/src/assets/images/cards/CardDebet.svg" ></CardDescription>
    <OrderFormDebit></OrderFormDebit>
</template>