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
        <div class="transition p-bottom-xxs">
        <v-card class="rounded-lg width-200 height-180 bg-cl">
            <v-card-item>
                <img :src="fImgLink" class="img-guide__first">
                <v-card-title>{{fCardTitle}}</v-card-title>
                <v-card-subtitle>{{fCardDescription}}</v-card-subtitle>
            </v-card-item>
        </v-card>
    </div>
    <div class="transition p-bottom-xxs">
        <v-card class="rounded-lg width-200 height-180 bg-cl">
            <v-card-item>
                <img :src="sImgLink" class="img-guide__second">
                <v-card-title>{{sCardTitle}}</v-card-title>
                <v-card-subtitle>{{sCardDescription}}</v-card-subtitle>
            </v-card-item>
        </v-card>
    </div>
    <div class="transition">
        <v-card class="rounded-lg width-200 height-180 bg-cl">
            <v-card-item>
                <img :src="tImgLink" class="img-guide__third">
                <v-card-title>{{tCardTitle}}</v-card-title>
                <v-card-subtitle>{{tCardDescription}}</v-card-subtitle>
            </v-card-item>
        </v-card>
    </div>
</div>
</div>
</template>

<style lang="scss">
.welcome-guide {
    display: flex;
    flex-direction: column;
    
    h2 {
        font-size: 1.5rem;
        text-align: center;
        padding-bottom: 3%;
        word-spacing: 3px;

        @include large {
            font-size: 1.9rem;
        }
        @include medium {
            font-size: 1.2rem;
        }
        @include small {
            font-size: 1.2rem;
        }
        @include extra-small {
            font-size: 1.3rem;
        }
        @include x-extra-small {
            font-size: 0.8rem;
        }
    }
    .welcome-cards {
        display: flex;
        justify-content: space-around;
    
        @include small {
            flex-direction: column;
            align-items: center;
        }
        @include extra-small {
            flex-direction: column;
            align-items: center;
        }
    }
}
.img-guide__first {
  width: 30% ;
  height: 30%;
    @include large {
        padding-bottom: 2%;
    }
    @include extra-small {
        padding-bottom: 8%;
    }
}

.img-guide__second {
    width: 45%;
    height: 60%;
    margin-bottom: 8%;
}

.img-guide__third {
    width: 50%;
    height: 70%;
    margin: 10% 10% 11% 10%;
}

.v-card--variant-elevated, .v-card--variant-flat {
    color: white !important;
}

.v-card-item__content {
    display: flex;
    flex-direction: column;
    align-items: center;

    .v-card-title {
        font-size: 1rem;

        @include large {
            font-size: 1.3rem;    
        }
        @include medium {
            font-size: 1rem;    
        }
        @include small {
            font-size: 0.8rem;    
        }
        @include extra-small {
            font-size: 0.8rem;    
        }
    }

    .v-card-subtitle {
        white-space: normal !important;
        text-align: center;

        @include large {
            font-size: 1.1rem;    
        }
        @include medium {
            font-size: 0.8rem;    
        }
        @include small {
            font-size: 0.6rem;    
        }
        @include extra-small {
            font-size: 0.7rem;    
        }
    }
}

.transition {
    transition: transform .4s cubic-bezier(0,0,.4,1);

    &:hover {
        transform: scale3d(1.03,1.03,1.03);
    }
}

.bg-cl {
    background: #154acf26 !important;
}

.p-bottom-xxs {
    padding-bottom: 3%;
}
.width-200 {
    @include large {
        width: 22rem;
    }
    @include medium {
        width: 18rem;
    }
    @include extra-small {
        width: 15rem;    
    }
    @include x-extra-small {
        width: 10rem;    
    }
}

.height-180 {
    height: 12rem;

    @include large {
        height: 18rem;
    }
    @include medium {
        height: 16rem;    
    }
    @include extra-small {
        height: 14rem;    
    }
    @include x-extra-small {
        height: 12rem;    
    }
}
</style>