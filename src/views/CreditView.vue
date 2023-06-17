<script setup>
import CardsTitle from '../components/cards/CardsTitle.vue';
import CardDescription from '../components/cards/CardDescription.vue';
import OrderFormCredit from '../components/cards/OrderFormCredit.vue';
import GuidesMain from '../components/GuidesMain.vue';
</script>

<template>
  <CardsTitle 
  cardType="Credit" 
  cardDescription="Allows you to pay for purchases at the expense of the bank. Pay with a card and get cashback for any purchases"></CardsTitle>
  <CardDescription 
  cardName="Aurora" 
  description="Using credit card you can buy whatever you want with special offers" 
  imgLink="../../public/images/cards/CardCredit.svg"></CardDescription>
  <GuidesMain 
  pageTitle="Conditions" 
  fCardTitle="Cashback" 
  fCardDescription="Up to 30% of cashback from each payment" 
  fImgLink="../../public/images/icons/cards-description/cashback.svg" 
  sCardTitle="Deposit" 
  sCardDescription="Up to 5% annual for saving on your card" 
  sImgLink="../../public/images/icons/cards-description/deposit.svg" 
  tCardTitle="Commission" 
  tCardDescription="No taxes and fees for using your cards" 
  tImgLink="../../public/images/icons/cards-description/commission.svg"></GuidesMain>
  <OrderFormCredit></OrderFormCredit>
</template>