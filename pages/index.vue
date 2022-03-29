<template>
  <!-- Index page, or Home page. Must no be confused with default page.
       This page is injected into the default page and displays where the <Nuxt /> tag is placed.
   -->
  <div>
    <v-toolbar color="" flat height="78">
      <v-img src="/logo.png" max-width="250"></v-img>
      <v-spacer></v-spacer>
      <div class="hidden-sm-and-down">
        Tel: 056-515-1309
        <v-icon class="mb-1" color="darkgreen" small>mdi-circle</v-icon>
        Sales: 083-256-8151
        <v-icon class="mb-1" color="darkgreen" small>mdi-circle</v-icon>
        email: pa@emilling.co.za
      </div>
      <v-spacer></v-spacer>
      <v-btn class="hidden-sm-and-down" icon href="https://www.facebook.com" target="_blank">
        <v-icon color="blue" x-large>mdi-facebook</v-icon>
      </v-btn>
      <v-btn class="hidden-sm-and-down" icon>
        <v-icon color="green" x-large>mdi-whatsapp</v-icon>
      </v-btn>
      <v-btn class="hidden-sm-and-down" icon>
        <v-icon color="purple" x-large>mdi-instagram</v-icon>
      </v-btn>
    </v-toolbar>
    <v-img class="hidden-sm-and-down" src="/office.jpg">
      <v-row>
        <v-col
          cols="12"
          lg="8"
          md="8"
        >
          <v-card
            class="intro-text pa-2 mt-6 ml-6 hidden-md-and-down"
            flat
            dark
          >
            <h2>eendag Meule is a state of the art Maize Mill, situated in the Maize
              capital of South Africa. We purchase 100% of our raw materials locally.</h2>
          </v-card>
        </v-col>
        <ContactForm />
      </v-row>
    </v-img>
    <v-card class="ma-4 pa-2 text-center hidden-md-and-up">
      <v-btn class="hidden-md-and-up" icon href="https://www.facebook.com" target="_blank">
        <v-icon color="blue" x-large>mdi-facebook</v-icon>
      </v-btn>
      <v-btn class="hidden-md-and-up" icon>
        <v-icon color="green" x-large>mdi-whatsapp</v-icon>
      </v-btn>
      <v-btn class="hidden-md-and-up" icon>
        <v-icon color="purple" x-large>mdi-instagram</v-icon>
      </v-btn>
    </v-card>
    <h4 class="ma-6 hidden-sm-and-up">eendag Meule is a state of the art Maize Mill, situated in the Maize capital of South Africa. We purchase 100% of our raw materials locally.</h4>
    <ContactForm  class="hidden-sm-and-up"/>
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
      <h1 class="grey--text text--darken-2 hidden-sm-and-down"><i>"With unrivalled speed and reliability, Our systems provides a peace of mind packing solution to
        continuously pack our maize meal, and deliver on time."</i></h1>
      <h4 class="grey--text text--darken-2 hidden-md-and-up"><i>"With unrivalled speed and reliability, Our systems provides a peace of mind packing solution to
        continuously pack our maize meal, and deliver on time."</i></h4>
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
  background-color: rgba(0, 0, 0, 0.2) !important;
}

.product-range {
  background-color: rgba(0, 0, 0, 0.2) !important;
}

.contact-form {
  background-color: rgba(255, 255, 255, .15) !important;
  backdrop-filter: blur(3px);
}
</style>
