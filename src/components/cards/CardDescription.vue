<script>
export default {
    props: {
      cardName: String,
      description: String,
      imgLink: String,
    }
  }
</script>

<template>
    <div class="debit__welcome-container">
        <v-col cols="11">
          <v-card
            color="#154acf26"
            theme="dark"
            class="rounded-lg"
          >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title class="text-body-1 text-uppercase">
                  {{cardName}}
                </v-card-title>

                <v-card-subtitle
                class="text-body-2">
                {{description}}
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
                <img :src="imgLink" alt="Debit Card">
              </v-avatar>
            </div>
          </v-card>
        </v-col>   
      </div>
</template>

<style lang="scss">
.debit__welcome-container {
  padding-bottom: 3%;
}
.text-body-2 {
    white-space: normal;
    padding: 0 2rem;
}

.img-guide__second {
    width: 29%;
    height: 30%;
    padding-bottom: 0;
}

.img-guide__third {
  width: 30%;
  height: 30%;
  margin: 3%;
}

.welcome-guide {
  height: 55vh;
}
</style>