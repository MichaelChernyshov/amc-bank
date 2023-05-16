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
            <v-btn variant="plain" size="x-small">Normal</v-btn>
            <v-btn variant="plain" size="x-small">Premium</v-btn>
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
    justify-content: space-around;
    background-color: grey;
    width: 40%;
}
</style>