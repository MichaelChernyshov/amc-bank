<script>
import DepositeEveryone from './DepositeEveryone.vue';
import DepositePremium from './DepositPremium.vue';
  export default {
    data: () => ({
      everyone: true,
      premium: false,
    }),
    components: {
      DepositeEveryone,
      DepositePremium
    }
  }
</script>

<template>
    <v-maim>
<div class="d-flex flex-row justify-space-around align-center">
        <div class=" ml-15 w-auto">
            <div>
                <h1 class="text-lg-h2 text-md-h3 text-sm-h4">Deposit</h1>
                <h2 class="text-lg-h3 text-md-h4 text-sm-h5">Save your money safely</h2>
            </div>
        </div>

        <div class="ma-4 w-50 d-flex justify-center align-center">
          <img src="/src/assets/images/icons/deposit.svg" alt="Deposit icon" class="try">
        </div>
    </div>


<v-container class="d-flex justify-left align-center">
  <h1 class="text-h5 pr-5">Choose variants: </h1>
  <v-tabs class="text-h1">
    <v-tab @click="everyone = true; premium = false" class="text-h5" mandatory="true">For everyone</v-tab>
    <v-tab @click="premium = true; everyone = false" class="text-h5">For premium</v-tab>
  </v-tabs>
</v-container>
<div>
    <DepositeEveryone v-if="everyone" />
    <DepositePremium v-if="premium"/>
  </div>
</v-maim>
</template>

<style lang="scss">
.try {
  width: 70%;
  height: 50%;
}
</style>