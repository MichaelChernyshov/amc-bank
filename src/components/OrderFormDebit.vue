<script>
  import { ref } from 'vue'
  import { useField, useForm } from 'vee-validate'

  export default {
    setup () {
      const { handleReset } = useForm({
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
        'Usual Debit',
        'Premium Debit',
      ])

      const submit = function () {
        handleReset()
        alert("You have successfully ordered our card.")
      }

      return { name, phone, email, select, checkbox, items, submit, handleReset }
    },
  }
</script>

<template>
  <section class="section__order">
    <form @submit.prevent="submit" class="order-form">
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
  </section>
  </template>

<style lang="scss">
.section__order {
  display: flex;
  justify-content: center;

  .order-form {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 60%;
    padding: 5%;
    background-color: rgba(21, 74, 207, 0.15);
    border-radius: 10px;
}
}

.v-field__field {

  label {
    font-size: 8px;
  }
  input {
    font-size: 8px;
    min-height: 8px;
  }
}

.v-field--active {
  font-size: 10px;
}

.v-fiel-label {
  top: 1px;
}
// .v-input__prepend {
//   i {

//   }
// }

.v-input--density-default {
  padding-top: 0;
}

.v-selection-control {
  label {
    font-size: 10px;
  }
}
.buttons {
  button {
    span {
      font-size: 11px;
      padding: 5px;
      color: black;
    }
  }
}
</style>