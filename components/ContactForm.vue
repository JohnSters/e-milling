<template>
  <v-card
    class="xs7"
    flat
  >
    <h3 class="text-center">Have any questions? Let us contact you.</h3>
    <v-form
      ref="form"
      v-model="valid"
      lazy-validation
    >
      <v-text-field
        v-model="name"
        :counter="10"
        :rules="nameRules"
        label="Name"
        required
      ></v-text-field>

      <v-text-field
        label="Number"
        required
      ></v-text-field>

      <v-text-field
        v-model="email"
        :rules="emailRules"
        label="E-mail"
        required
      ></v-text-field>

      <v-textarea
        label="Short Message"
      ></v-textarea>

      <v-checkbox
        label="Receive News Letter?"
        required
      ></v-checkbox>

      <v-btn
        :disabled="!valid"
        class="mr-4 hidden-sm-and-down"
        depressed
        @click="validate"
      >
        Contact Me
      </v-btn>
      <v-btn
        :disabled="!valid"
        class="mr-4 hidden-sm-and-down"
        depressed
        @click="validate"
      >
        Download Brochure
      </v-btn>

      <v-btn
        :disabled="!valid"
        class="rounded-xl hidden-sm-and-up"
        depressed
        x-small
        @click="validate"
      >
        Contact Me
      </v-btn>
      <v-btn
        :disabled="!valid"
        class="rounded-xl hidden-sm-and-up"
        depressed
        x-small
        @click="validate"
      >
        Download Brochure
      </v-btn>

    </v-form>
  </v-card>
</template>

<script>
export default {
  name: "ContactForm",
  data: () => ({
    valid: true,
    name: '',
    nameRules: [
      v => !!v || 'Name is required',
      v => (v && v.length <= 10) || 'Name must be less than 10 characters',
    ],
    email: '',
    emailRules: [
      v => !!v || 'E-mail is required',
      v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
    ],
  }),

  methods: {
    validate() {
      this.$refs.form.validate()
    },
    reset() {
      this.$refs.form.reset()
    },
    resetValidation() {
      this.$refs.form.resetValidation()
    },
  },
}
</script>

<style scoped>

</style>
