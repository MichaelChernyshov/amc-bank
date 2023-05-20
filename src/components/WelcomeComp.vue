<script setup>
</script>

<template>
<main class="main">
    <article class="main__main-info">
        <div class="main__description">
            <h1 class="main__welcome">Pay everywhere you want with a cashback</h1>
            <div>
            <v-btn variant="outlined" rounded="xl" size="x-small" prepend-icon="mdi-apple" class="mr-3">
                AppStore
            </v-btn>
            <v-btn variant="outlined" rounded="xl" size="x-small" prepend-icon="mdi-google-play">
              Google Play
            </v-btn>
        </div>
        </div>
            <img src="../assets/images/cards/done2.svg" alt="Two cards" class="two-cards__image">
    </article>
</main>
</template>

<style lang="scss">
.main {
    width: 100vw;
    height: 84vh;
    padding: 3%;
    display: flex;
    align-items: center;

    .main__main-info {
        display: flex;
        flex-direction: row;
        align-items: center;

        .main__description {
            display: flex;
            flex-direction: column;
            padding-left: 5%;
        }

        .main__welcome {
            max-width: 85%;
            word-spacing: 3px;
            font-size: 28px;
            font-weight: 300;
        }
    }
}

.two-cards__image {
    width: 43%;
    height: 40%;
}
</style>