<script>
export default {
  data: () => ({
      windowSize: {
        x: 0,
        y: 0,
      },
    }),
    mounted () {
      this.onResize()
    },
    props: {
      cardName: String,
      description: String,
      imgLink: String,
    },
    methods: {
      onResize () {
        this.windowSize = { x: window.innerWidth, y: window.innerHeight }
      },
    },
  }
</script>

<template>
    <div class="debit__welcome-container">
        <v-col cols="11" class="card-hover">
          <v-card
            color="#154acf26"
            theme="dark"
            class="rounded-lg card-hover-two"
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
      <v-row
    v-resize="onResize"
    align="center"
    justify="center"
  >
    <v-col class="text-center">
      <div class="text-subtitle-2">Window Size</div>
      {{ windowSize }}
    </v-col>
  </v-row>
</template>

<style lang="scss">
.debit__welcome-container {
  padding-bottom: 3%;
}
.text-body-2 {
    white-space: normal;
    padding: 0 2rem;
}

.img-guide__first {
  width: 30%;
  height: 30%;
  margin: 3%;
  padding-bottom: 3%;
}

.img-guide__second {
    width: 30%;
    height: 20%;
    padding-bottom: 2%;
    margin: 3%;
}

.img-guide__third {
  width: 30%;
  height: 30%;
  margin: 3%;
  padding-bottom: 9%;
}
.card-hover {
  transition: transform .4s cubic-bezier(0,0,.4,1);

  &:hover {
    transform: scale3d(1.04,1.04,1.04);
  }
}

.height-180 {
    height: 12rem;

    @include large {
        height: 15rem;    
    }
    @include medium {
        height: 12rem;    
    }
    @include small {
        height: 10rem;    
    }
    @include extra-small {
        height: 11rem;    
    }
    @include x-extra-small {
        height: 11.2rem;    
    }
}

.width-200 {
  @include large {
    width: 21rem;    
  }
  @include medium {
    width: 17rem;    
  }
  @include small {
      width: 12rem;    
  }
  @include extra-small {
      width: 14rem;    
    }
}
</style>