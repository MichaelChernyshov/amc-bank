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

        <img src="../assets/images/cards/CardDebet.svg" alt="Debit Card" class="debit__card">
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
        font-size: 28px;
        font-weight: 300;
        word-spacing: 3px;
    }

    p {
        text-align: center;
        font-weight: 300;
        word-spacing: 2px;
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
}

.debit__card {
    width: 250px;
    height: 150px;
}
</style>