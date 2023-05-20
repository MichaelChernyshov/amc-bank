<script>
export default {
    props: {
      cardType: String,
      cardDescription: String,
    }
  }
</script>

<template>
    <section class="debit__welcome-container">
    <article class="card__welcome">
            <h1>{{cardType}} cards</h1>
            <p>{{cardDescription}}</p>
        </article>
    </section>
</template>

<style lang="scss">
.debit__welcome-container {
    display: flex;
    flex-direction: column;
    align-items: center;
}
.card__welcome {
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
</style>