<script>
export default {
    props: {
      cardName: String,
      description: String,
      imgLink: String,
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
                rounded="0"
              >
                <img :src="imgLink" alt="Debit Card" class="img-size">
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

.mt-5 {
  @include extra-small {
      margin-top: 0 !important;    
    }
}

.d-flex {
  align-items: center;
  @include extra-small {
    flex-direction: column;
    align-items: center;
  }
}
.mr-9 {
  @include extra-small {
    margin-right: 0 !important;
  }
}
.v-avatar {
  width: 170px !important;
  height: 110px !important;

  @include large {
    width: 270px !important;
    height: 220px !important;
  }
  @include medium {
    width: 220px !important;
    height: 170px !important;
  }
  @include small {
    font-size: 1.2rem !important;
  }
}

.v-col, .v-col-11 {
  padding: 0;
  @include extra-small {
    max-width: 60% !important;
  }
}

.v-card .v-card-title {
  @include extra-small {
    text-align: center;
  }
}

.v-card {
  padding: 10px;
}

.text-body-1 {
  @include large {
    font-size: 1.6rem !important;
  }
  @include medium {
    font-size: 1.5rem !important;
  }
  @include small {
    font-size: 1.2rem !important;
  }
}

.text-body-2 {
  @include large {
    font-size: 1.4rem !important;
  }
  @include medium {
    font-size: 1.3rem !important;
  }
  @include small {
    font-size: 1rem !important;
  }
}

.v-btn--size-x-small{
  @include large {
    font-size: 1.2rem !important;
  }
  @include medium {
    font-size: 1rem !important;
  }
  @include small {
    font-size: 0.8rem !important;
  }
}
</style>