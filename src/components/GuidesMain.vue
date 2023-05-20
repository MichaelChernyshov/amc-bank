<script>
export default {
    props: {
      pageTitle: String,
      fImgLink: String,
      fCardTitle: String,
      fCardDescription: String,
      sImgLink: String,
      sCardTitle: String,
      sCardDescription: String,
      tImgLink: String,
      tCardTitle: String,
      tCardDescription: String,
    }
  }
</script>

<template>
<div class="welcome-guide">
    <h2>{{ pageTitle }}</h2>
    <div class="welcome-cards">
        <v-card width="200" class="rounded-lg">
            <v-card-item>
                <img :src="fImgLink" class="img-guide__first">
                <v-card-title>{{fCardTitle}}</v-card-title>
                <v-card-subtitle>{{fCardDescription}}</v-card-subtitle>
            </v-card-item>
        </v-card>

        <v-card width="200" class="rounded-lg">
            <v-card-item>
                <img :src="sImgLink" class="img-guide__second">
                <v-card-title>{{sCardTitle}}</v-card-title>
                <v-card-subtitle>{{sCardDescription}}</v-card-subtitle>
            </v-card-item>
        </v-card>

        <v-card width="200" class="rounded-lg">
            <v-card-item>
                <img :src="tImgLink" class="img-guide__third">
                <v-card-title>{{tCardTitle}}</v-card-title>
                <v-card-subtitle>{{tCardDescription}}</v-card-subtitle>
            </v-card-item>
        </v-card>
</div>
</div>
</template>

<style lang="scss">
.welcome-guide {
    display: flex;
    flex-direction: column;
    height: 85vh;
    
    h2 {
        font-size: 22px;
        text-align: center;
        padding-bottom: 3%;
        word-spacing: 3px;
    }
    .welcome-cards {
        display: flex;
        justify-content: space-around;
    }
}
.img-guide__first {
  width: 30% ;
  height: 30%;
}

.img-guide__second {
    width: 45%;
    height: 60%;
    padding-bottom: 9%;
}

.img-guide__third {
    width: 50%;
    height: 70%;
    margin: 10% 10% 11% 10%;
}

.v-card--variant-elevated, .v-card--variant-flat {
    background: #154acf26 !important;
    color: white !important;
}

.v-card-item__content {
    display: flex;
    flex-direction: column;
    align-items: center;

    .v-card-title {
        font-size: 13px !important;
    }

    .v-card-subtitle {
        font-size: 10px !important;
        white-space: normal !important;
        text-align: center;
    }
}
</style>