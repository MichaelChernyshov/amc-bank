<script setup>
import CardsTitle from '../components/cards/CardsTitle.vue';
import CardDescription from '../components/cards/CardDescription.vue';
import OrderFormDebit from '../components/cards/OrderFormDebit.vue';
// import CardsButtons from '../components/CardsButtons.vue'
import GuidesMain from '../components/GuidesMain.vue';
</script>

<template>
    <CardsTitle cardType="Debit" cardDescription="Using debit card is the best way to pay for everything you want and after all - receive a cashback"></CardsTitle>
    <!-- <CardsButtons cardName="4U Debit" cardType="Debit"></CardsButtons> -->
    <CardDescription cardName="Galaxy" description="Debit card that you can use everywhere you want and take all advantages of it without any problems" imgLink="/assets/images/cards/CardDebet.svg" ></CardDescription>
    <GuidesMain pageTitle="Conditions" fCardTitle="Cashback" fCardDescription="Up to 15% of cashback from each payment" fImgLink="/assets/images/icons/cards-description/cashback.svg" sCardTitle="Deposit" sCardDescription="Up to 2% annual for saving on your card" sImgLink="/assets/images/icons/cards-description/deposit.svg" tCardTitle="Commission" tCardDescription="No taxes and fees for using your cards" tImgLink="/assets/images/icons/cards-description/commission.svg"></GuidesMain>
    <OrderFormDebit></OrderFormDebit>
</template>