<template>
  <v-app>
    <v-app-bar>
      <v-card
          color="#e1e1e1"
          class="ma-auto mt-5 pa-5"
          width="500px"
          elevation="7"
      >
        <v-form
            color="blue"
            ref="form"
            v-model="valid"
            lazy-validation
        >
          <v-text-field
              v-model="email"
              :rules="emailRules"
              label="Login"
              required
          ></v-text-field>

          <v-text-field
              v-model="password"
              :append-icon="show1 ? 'mdi-eye' : 'mdi-eye-off'"
              :type="show1 ? 'text' : 'password'"
              label="Password"
              @click:append="show1 = !show1"
          ></v-text-field>

          <v-btn
              :disabled="!valid"
              color="#0082ca"
              class="mr-4"
              @click="validate"
          >
            Login
          </v-btn>
        </v-form>
      </v-card>
    </v-app-bar>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    password: '',
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
    ],
    select: null
  }),

  methods: {
    validate() {
      this.$refs.form.validate()
    }
  },
}
</script>
<style>
.v-btn__content {
  color: white;
}
.v-btn:hover {
  color:rgb(64 191 239);
}
</style>

