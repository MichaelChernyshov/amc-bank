<script>
export default {
    props: {
      cardName: String,
      cardType: String,
    }
  }
</script>

<template>
    <section class="debit__welcome-container">
        <section class="debit__buttons">
            <v-btn variant="plain" size="x-small">{{ cardName }}</v-btn>
            <v-divider vertical></v-divider>
            <v-btn variant="plain" size="x-small">Premium {{ cardType }}</v-btn>
        </section>
    </section>
</template>

<style lang="scss">
.debit__buttons {
    display: flex;
    justify-content: space-evenly;
    background-color: rgba(128, 128, 128, 0.5);
    border: 1px solid grey;
    border-radius: 10px;
    margin-bottom: 2%;
}
.v-btn--size-x-small {
    padding: 0 15px;
}
</style>