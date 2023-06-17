<script setup>
</script>

<template>
<div class="main">
    <article class="main__main-info">
        <div class="main__description">
            <h1 class="main__welcome">Pay everywhere you want with cashback</h1>
            <div class="download-buttons">
            <v-btn variant="outlined" rounded="xl" prepend-icon="mdi-apple" class="mr-3">
                AppStore
            </v-btn>
            <v-btn variant="outlined" rounded="xl" prepend-icon="mdi-google-play">
              Google Play
            </v-btn>
        </div>
        </div>
            <img src="../../../public/images/cards/done2.svg" alt="Two cards" class="two-cards__image">
    </article>
</div>
</template>

<style lang="scss">
.main {
    width: 100vw;
    align-items: center;

    .main__main-info {
        display: flex;
        flex-direction: row;
        align-items: center;

        @include extra-small {
            display: flex;
            flex-direction: column
        }

        .main__description {
            display: flex;
            flex-direction: column;
            padding: 0 5%;

            @include extra-small {
                padding: 3%;
                align-items: center;
            }
        }

        .main__welcome {
            word-spacing: 3px;
            font-weight: 300;
            padding-bottom: 2%;

            @include large {
                font-size: 3rem;
                max-width: 60%;
            }
            @include medium {
                font-size: 2rem;
                max-width: 60%;
            }
            @include small {
                font-size: 1.7rem;
                max-width: 60%;
            }
            @include extra-small {
                font-size: 1.5rem;
                max-width: 100%;
                text-align: center;
            }
            @include x-extra-small {
                font-size: 1rem;
                max-width: 100%;
                text-align: center;
            }
        }
    }
}
.download-buttons {
    display: flex;
    flex-direction: row;
    align-items: start;
}
.two-cards__image {
    width: 50%;
    @include large {
        max-width: 38%;
    }
    @include medium {
        max-width: 40%;
    }
    @include small {
        max-width: 38%;
    }
    @include extra-small {
        max-width: 70%;
    }
    @include x-extra-small {
        max-width: 50%;
    }

}

.v-btn--size-default {
    
    @include small {
        font-size: 0.45rem;
    }
    @include x-extra-small {
        font-size: 0.4rem;
        padding: 0 0.8rem;
        height: 1.5rem !important;
    }
}
</style>