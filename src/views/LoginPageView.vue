<script>
  import { useField, useForm } from 'vee-validate'
    export default {
        setup () {
            let { message } = useForm({
        validationSchema: {
          email (value) {
            if (/^[a-z.-]+@[a-z.-]+\.[a-z]+$/i.test(value)) return true

            return 'Must be a valid e-mail.'
          },
        },
      })
      const email = useField('email')
      message = "successfully"

      return {email, message }
        },
    data: () => ({
      show1: false,
      show2: true,
      form: false,
      password: null,
      loading: false,
    }),

    methods: {
      onSubmit () {
        if (!this.form) return

        this.loading = true

        setTimeout(() => (
            this.loading = false,
            alert("You have logined successfully")
            ), 2000)
      },
      required (v) {
        return !!v || 'Field is required'
      },
    },
  }
</script>

<template>
<div class="login d-flex align-center justify-space-around">
    <div class="welcome-message">
        <h1 class="bank-welcome">We welcome you to your online bank account</h1>
    </div>
  <v-sheet class="pa-12" rounded>
    <v-card class="mx-auto px-6 py-8">
      <v-form
        v-model="form"
        @submit.prevent="onSubmit"
      >
        <v-text-field
          v-model="email.value.value"
          :error-messages="email.errorMessage.value"
          :readonly="loading"
          :rules="[required]"
          class="mb-2"
          label="Email"
          placeholder="Enter your email"
          variant="outlined"
        ></v-text-field>

        <v-text-field
          v-model="password"
          :readonly="loading"
          :rules="[required]"
          :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
          :type="show1 ? 'text' : 'password'"
          label="Password"
          placeholder="Enter your password"
          variant="outlined"
          @click:append="show1 = !show1"
        ></v-text-field>

        <br>

        <v-btn
          :disabled="!form"
          :loading="loading"
          block
          color="success"
          size="large"
          type="submit"
          variant="elevated"
        >
          Sign In
        </v-btn>
      </v-form>
    </v-card>
  </v-sheet>
</div>
</template>

<style lang="scss">
.welcome-message {
    width: 30%;
    display: flex;
}
.bank-welcome {
    font-size: 3rem;
    // width: 30%;
}
.v-sheet {
    background: none;
    width: 40%;
}
.login {
    height: 72vh;
}

.bg-success {
    background-color: rgb(26, 31, 183) !important;
}
.v-btn--disabled.v-btn--variant-elevated .v-btn__overlay, .v-btn--disabled.v-btn--variant-flat .v-btn__overlay {
    opacity: 0.1;
}
</style>