<script setup>
</script>

<template>
<main class="main">
    <article class="main__main-info">
        <h1 class="main__welcome">Pay everywhere you want with a cashback</h1>
        <div class="main__donload-buttons">
            <v-btn variant="outlined" rounded="xl" size="x-small" prepend-icon="mdi-apple" class="mr-3">
                AppStore
            </v-btn>
            <v-btn variant="outlined" rounded="xl" size="x-small" prepend-icon="mdi-google-play">
              Google Play
            </v-btn>
        </div>
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

        .main__welcome {
            max-width: 40%;
            word-spacing: 3px;
            font-size: $title-text-large;
            font-weight: 300;
        }
    }
}
</style>