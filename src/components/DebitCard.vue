<script>
export default {
    data: () => ({ value: 0 }),
  }
</script>

<template>
    <main class="debit__welcome-container">
        <article class="debit__welcome">
            <h1>Debit cards</h1>
            <p>Using debit card is the best way to pay for everything you want and after all - receive a cashback</p>
        </article>

        <section class="debit__buttons">
            <v-btn variant="plain" size="x-small">4U Debit</v-btn>
            <v-divider vertical></v-divider>
            <v-btn variant="plain" size="x-small">Premium Debit</v-btn>
        </section>

        <v-col cols="11">
          <v-card
            color="#154acf26"
            theme="dark"
            class="rounded-lg"
          >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title class="text-body-1">
                  4U Debit
                </v-card-title>

                <v-card-subtitle
                class="text-body-2">
                Debit card that you can use everywhere you want and take all advantages of it without any problems
                </v-card-subtitle>

                <v-card-actions class="mt-5">
                  <v-btn
                    class="ms-2"
                    variant="plain"
                    size="x-small"
                    href="#order"
                  >
                    Order
                  </v-btn>
                </v-card-actions>
              </div>

              <v-avatar
                class="mr-9"
                size="170"
                rounded="0"
              >
                <img src="../assets/images/cards/CardDebet.svg" alt="Debit Card">
              </v-avatar>
            </div>
          </v-card>
        </v-col>   
    </main>
</template>

<style lang="scss">
.debit__welcome-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100vw;
    height: 84vh;
}
.debit__welcome {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 70%;
    padding-bottom: 3%;
    
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
    margin-bottom: 2%;
}
.v-btn--size-x-small {
    padding: 0 15px;
}

.text-body-2 {
    white-space: normal;
    padding: 0 2rem;
}
</style>