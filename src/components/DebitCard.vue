<script>
export default {
    data: () => ({ value: 0 }),
  }
</script>

<template>
    <main class="debit__welcome-container">
        <article class="debit__welcome">
            <h1>Debit cards</h1>
            <p>Using debit card is the best way to pay for everything you want and after all - receive a cashback.</p>
        </article>

        <section class="debit__buttons">
            <v-btn variant="plain" size="x-small">Usual Debit</v-btn>
            <v-divider vertical></v-divider>
            <v-btn variant="plain" size="x-small">Premium Debit</v-btn>
        </section>
    </main>

</template>

<style lang="scss">
.debit__welcome-container {
    display: flex;
    flex-direction: column;
    align-items: center;
}
.debit__welcome {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 70%;
    padding-bottom: 2%;
    
    
    h1 {
        font-weight: 900;
    }

    p {
        text-align: center;
        font-weight: 300;
    }
}
.debit__buttons {
    display: flex;
    justify-content: space-evenly;
    background-color: rgba(128, 128, 128, 0.5);
    border: 1px solid grey;
    border-radius: 10px;
}
.v-btn--size-x-small {
    padding: 0 15px;
    border-radius: 10px;
}
</style>