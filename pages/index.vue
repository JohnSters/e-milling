<template>
  <!-- Index page, or Home page. Must no be confused with default page.
       This page is injected into the default page and displays where the <Nuxt /> tag is placed.
   -->
  <div>
    <v-toolbar color="" flat height="78">
      <v-img src="/logo.png" max-width="250"></v-img>
      <v-spacer></v-spacer>
      Tel: 056-515-1309
      <v-divider class="ml-2 mr-2" vertical></v-divider>
      Sales: 083-256-8151
      <v-divider class="ml-2 mr-2" vertical></v-divider>
      email: pa@emilling.co.za
      <v-spacer></v-spacer>
      <v-btn icon href="https://www.facebook.com" target="_blank">
        <v-icon color="blue" x-large>mdi-facebook</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon color="green" x-large>mdi-whatsapp</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon color="purple" x-large>mdi-instagram</v-icon>
      </v-btn>
    </v-toolbar>
    <v-img src="/office.jpg">
      <v-row>
        <v-col
          cols="12"
          sm="6"
          md="8"
        >
          <v-card
            class="intro-text pa-2 mt-6 ml-6"
            flat
          >
            <h1 class="grey--text text--darken-3">eendag Meule is a state of the art Maize Mill, situated in the Maize
              capital of
              South Africa. We purchase 100% of our raw materials locally.</h1>
          </v-card>
        </v-col>
        <v-col
          cols="6"
          md="4"
        >
          <v-card
            class="contact-form pa-4 mt-6 mr-6 rounded"
            flat
          >
            <h3 class="text-center">Want to find out more?</h3>
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

              <v-checkbox
                label="Receive News Letter?"
                required
              ></v-checkbox>

              <v-btn
                :disabled="!valid"
                class="mr-4"
                depressed
                @click="validate"
              >
                Contact Me
              </v-btn>
              <v-btn
                :disabled="!valid"
                class="mr-4"
                depressed
                @click="validate"
              >
                Download Brochure
              </v-btn>

            </v-form>
          </v-card>
        </v-col>
      </v-row>
    </v-img>
    <v-toolbar color="#148a5c" flat></v-toolbar>
    <v-parallax
      height="200"
      src="/silos.jpg"
    >
      <v-container><h1 class="product-range text-center font-weight-bold">View our range of top quality products</h1>
      </v-container>
    </v-parallax>
    <v-toolbar color="#148a5c" flat></v-toolbar>
    <!-- This is the home page products tab. This page have several component imports for the different products (niche, maize, feeds.) -->
    <ProductCategory/>
    <!-- END -->
    <v-container>
      <v-divider class="ma-3"></v-divider>
      <h1><i>"With unrivalled speed and reliability, Our systems provides a peace of mind packing solution to
        continuously pack our maize meal, and deliver on time."</i></h1>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
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

<style>
.intro-text {
  background-color: rgba(255, 255, 255, 0.2) !important;
}

.product-range {
  background-color: rgba(0, 0, 0, 0.2) !important;
}

.contact-form {
  background-color: rgba(255, 255, 255, .15) !important;
  backdrop-filter: blur(3px);
}
</style>
