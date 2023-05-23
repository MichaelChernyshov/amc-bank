<script setup>
import DepositTitle from '../components/deposit/DepositTitle.vue'
import QuestionsPanel from '../components/e-sim/QuestionsPanel.vue'
</script>

<template>
  <DepositTitle />
  <QuestionsPanel titleF="When and how are interest accrued on savings accounts?" 
    textF="Percents is calculated monthly. If you opened an account on March 15, then percents will come on April 15 - on the last day of the billing period. They will be credited to the minimum balance that was on your account during the month."
    titleS="How to close the deposit ahead of schedule? Will interest be charged if I withdraw money early?"
    textS="You can close the deposit at any convenient time. Keep in mind that if you terminate the deposit agreement ahead of schedule, you lose the right to receive interest - you can only count on the initial amount plus the bank's interest rate in case of early termination. It is lower than the interest rate on the deposit. For deposits opened until September 30, 2022 inclusive"
    titleT="Is there a commission for deposit replenishment?"
    textT="You can replenish the deposit without cash without restrictions. The minimum amount for cash replenishment is 100 euros."
    />
</template>

<style lang="scss">
</style>