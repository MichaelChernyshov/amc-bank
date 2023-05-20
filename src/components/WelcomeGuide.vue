<script>
export default {
    props: {
      imgLink: String,
      fCardTitle: String,
      fCardDescription: String,
    }
  }
</script>

<template>
<div class="welcome-guide">
    <h2>Using guide</h2>
    <div class="welcome-cards">
        <v-card width="200">
            <v-card-item>
                <img :src="imgLink" class="img-guide">
                <v-card-title>{{fCardTitle}}</v-card-title>
                <v-card-subtitle>{{fCardDescription}}</v-card-subtitle>
            </v-card-item>
        </v-card>

        <v-card width="200">
            <v-card-item>
                <img :src="imgLink" class="img-guide">
                <v-card-title>{{fCardTitle}}</v-card-title>
                <v-card-subtitle>{{fCardDescription}}</v-card-subtitle>
            </v-card-item>
        </v-card>

        <v-card width="200">
            <v-card-item>
                <img :src="imgLink" class="img-guide">
                <v-card-title>{{fCardTitle}}</v-card-title>
                <v-card-subtitle>{{fCardDescription}}</v-card-subtitle>
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
.img-guide {
  width: 30% ;
  height: 30%;
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