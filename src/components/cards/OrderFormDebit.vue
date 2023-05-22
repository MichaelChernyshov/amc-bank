<script>
  import { ref } from 'vue'
  import { useField, useForm } from 'vee-validate'

  export default {
    setup () {
      const { handleSubmit, handleReset } = useForm({
        validationSchema: {
          name (value) {
            if (value) return true

            return 'Name needs to be filled.'
          },
          phone (value) {
            if (value?.length > 8 && /[0-9-]+/.test(value)) return true

            return 'Phone number needs to be at least 9 digits.'
          },
          email (value) {
            if (/^[a-z.-]+@[a-z.-]+\.[a-z]+$/i.test(value)) return true

            return 'Must be a valid e-mail.'
          },
          select (value) {
            if (value) return true

            return 'Select an item.'
          },
          checkbox (value) {
            if (value === '1') return true

            return 'Must be checked.'
          },
        },
      })
      const name = useField('name')
      const phone = useField('phone')
      const email = useField('email')
      const select = useField('select')
      const checkbox = useField('checkbox')

      const items = ref([
        'Galaxy Debit Card',
      ])

      const submit = handleSubmit(values => {
        alert("You've ordered card.", values)
        handleReset()
      })

      return { name, phone, email, select, checkbox, items, submit, handleReset }
    },
  }
</script>

<template>
  <section class="card-order">
  <div class="section__order" id="order">
    <form @submit.prevent="submit" class="order-form" >
      <h6>Order our credit card here</h6>
      <v-text-field
        v-model="name.value.value"
        :error-messages="name.errorMessage.value"
        prepend-icon="mdi-account"
        label="Name And Surname"
        variant="underlined"
        class="w-75"
      ></v-text-field>
  
      <v-text-field
        v-model="phone.value.value"
        :counter="15"
        :error-messages="phone.errorMessage.value"
        prepend-icon="mdi-phone"
        label="Phone Number"
        variant="underlined"
        class="w-75"
      ></v-text-field>
  
      <v-text-field
        v-model="email.value.value"
        :error-messages="email.errorMessage.value"
        prepend-icon="mdi-email"
        label="E-mail"
        variant="underlined"
        class="w-75"
      ></v-text-field>
  
      <v-select
        v-model="select.value.value"
        :items="items"
        :error-messages="select.errorMessage.value"
        prepend-icon="mdi-card-multiple"
        label="Select Card"
        variant="underlined"
        class="w-75"
      ></v-select>
  
      <v-checkbox
        v-model="checkbox.value.value"
        :error-messages="checkbox.errorMessage.value"
        value="1"
        label="I have read and agreed to the terms and Conditions"
        type="checkbox"
        class="w-75"
      ></v-checkbox>
  
      <div class="buttons">
      <v-btn
        class="me-4"
        type="submit"
        size="xs-small"
      >
        submit
      </v-btn>
  
      <v-btn @click="handleReset"
      size="xs-small"
      >
        clear
      </v-btn>
    </div>
    </form>
  </div>
</section>
  </template>

<style lang="scss">
.card-order {
  padding-top: 5%;
}
.section__order {
  display: flex;
  justify-content: center;

  .order-form {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 55%;
    padding: 3% 2% 2%;
    background-color: rgba(21, 74, 207, 0.15);
    border-radius: 10px;

    @include large {
        width: 60%;
      }
    @include medium {
        width: 70%;
      }
      @include extra-small {
        width: 80%;
      }

    h6 {
      padding-bottom: 1%;
      text-align: center;

      @include large {
        font-size: 2rem;
      }
      @include extra-small {
        font-size: 1rem;
      }
    }
}
}

.v-field__field {

  label {
    font-size: 8px;

    @include large {
        font-size: 20px;
    }
    @include extra-small {
      font-size: 14px;
      }
  }
  input {
    font-size: 8px;
    min-height: 8px;

    @include large {
        font-size: 25px;
      }
      @include extra-small {
      font-size: 14px;
      }
  }
}

.v-field--active {
  font-size: 10px;

  @include large {
        font-size: 18px;
  }
  @include extra-small {
        font-size: 14px;
  }
}

.v-field__input {
  --v-input-control-height: 25px !important;
}

.v-input--density-default {
  --v-input-padding-top: 5px !important;
  --v-input-control-height: 10px !important;

  @include large {
    --v-input-padding-top: 25px !important;
    --v-input-control-height: 10px !important;
  }
  @include extra-small {
    --v-input-padding-top: 10px !important;
    --v-input-control-height: 10px !important;
  }
}

.v-counter {
  font-size: 7px; 

  @include large {
    font-size: 20px;
  }
  @include extra-small {
    font-size: 5px;
  }
}

.v-messages {
  font-size: 7px;
}

.v-selection-control {
  label {
    font-size: 8px;

    @include large {
    font-size: 20px;
    }
    @include extra-small {
    font-size: 10px;
  }
  }
}
.buttons {
  button {
    span {
      font-size: 8px;
      padding: 5px;
      color: black;

      @include large {
        font-size: 20px; 
      }
      @include medium {
        font-size: 14px; 
      }
      @include small {
        font-size: 14px; 
      }
      @include extra-small {
        font-size: 14px;
      }
      @include x-extra-small {
        font-size: 12px;
      }
    }
  }
}
.v-overlay__content {
  max-height: 100px;
  max-width: 200px;
  min-width: 30px;
}

.v-list-item--density-default.v-list-item--one-line {
  min-height: 20px;

  @include large {
    min-height: 60px;
  }
  @include extra-small {
    min-height: 30px;
  }
}

.v-list-item-title {
  font-size: 8px;
  @include large {
    font-size: 20px;
  }
  @include extra-small {
    font-size: 15px;
  }
}

.v-icon--size-default {
  font-size: 15px;

  @include large {
    font-size: 30px;
  }
  @include extra-small {
    font-size: 20px;
  }
}

.v-input__prepend, .v-input__append {
  padding-top: 35px;
  @include extra-small {
    padding-top: 10px;
  }
}

.v-field--variant-plain.v-field, .v-field--variant-underlined.v-field {
  --v-field-padding-top: 5px;
}
</style>