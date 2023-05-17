<script setup>
</script>

<template>
<main class="main">
    <article class="main__main-info">
        <h1 class="main__welcome">Pay everywhere you want with a cashback</h1>
        <figure class="cube">
        </figure>
    </article>
</main>

<div class="try-div">
    <img src="../assets/images/icons/iphone-icon.svg" alt="Card Credit" class="try">
    <img src="../assets/images/icons/CardsQQ.svg" alt="" class="try">
</div>

<v-btn prepend-icon="mdi-apple">
  Button
</v-btn>
<v-btn prepend-icon="mdi-google">
  Button
</v-btn>
</template>

<style lang="scss">

.try {
    width: 30%;
    height: 30%;
}

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
            font-family: 'Poppins', sans-serif;
            font-weight: 300;
        }
    }
}

// .credit {
//     width: 210px;
//     height: 130px;
//     transform: scaleX(1.1) scaleY(1.1) scaleZ(1) rotateX(41deg) rotateY(-7deg) rotateZ(10deg) translateX(16px) translateY(-2px) translateZ(0px) skewX(0deg) skewY(0deg);
// }

// .cube {
// perspective: 1000px;
// perspective-origin: 50% 50%;
// }

// .shadow {
//     box-shadow: 0px 0px 30px 30px rgba(42, 186, 199, 0.3);
// }
</style>