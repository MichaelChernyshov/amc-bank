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

    @include large {
        font-size: 50px;
    }
    @include medium {
        font-size: 35px;
      }
      @include small {
        font-size: 25px;
      }
      @include extra-small {
        font-size: 20px;;
      }
      @include x-extra-small {
        font-size: 20px;
      }
    }

    p {
        text-align: center;
        font-weight: 300;
        word-spacing: 2px;

      @include large {
        font-size: 30px;
      }
      @include medium {
        font-size: 20px;
      }
      @include small {
        font-size: 15px;
      }
      @include extra-small {
        font-size: 10px;;
      }
      @include x-extra-small {
        font-size: 10px;
      }
    }
}
</style>