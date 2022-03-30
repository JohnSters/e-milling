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
    <v-carousel height="85vh" interval="9000" continuous :show-arrows="false" hide-delimiter-background hide-delimiters cycle>
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
      >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <v-card class="intro-text ma-6 pa-6 rounded-xl" dark>
            <h1><i>"{{ item.msg }}"</i></h1>
          </v-card>
        </v-row>
      </v-carousel-item>
    </v-carousel>
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
    <br>
    <v-row
      class="fill-height"
      align="center"
      justify="center"
    >
      <v-card class="pa-lg-4" width="500">
        <ContactForm />
      </v-card>
    </v-row>
    <v-container>
      <v-divider class="ma-3"></v-divider>
      <h1 class="grey--text text--darken-2 text-center hidden-sm-and-down"><i>"Eendag Meule Bothaville (Pty) Ltd is driven by customer satisfaction and we strive to keep customer relations strong by supplying the best range of quality products at competitive prices."</i></h1>
      <h4 class="grey--text text--darken-2 text-center hidden-md-and-up"><i>"Eendag Meule Bothaville (Pty) Ltd is driven by customer satisfaction and we strive to keep customer relations strong by supplying the best range of quality products at competitive prices."</i></h4>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data: () => ({
    valid: true,
    name: '',
    items: [
      {
        src: '/office.jpg', msg: 'Eendag Meule is an advanced Maize Mill, situated in the Maize capital of South Africa. We purchase 100% of our raw materials locally.'
      },
      {
        src: '/factory-inside.jpg', msg: 'Eendag Meule recently installed a Westweigh Systems; fully automatic - Premiertech (Chronos bag) placing system. This makes us the first mill in South Africa to install such a bagging system.'
      },
      {
        src: '/office-inside.jpg', msg: 'With unrivalled speed and reliability, Our systems provides a peace of mind packing solution to continuously pack our maize meal, and deliver on time.'
      },
      {
        src: '/machinery6.jpg', msg: 'With packing speeds of 20 bags/min for 10kg and 12.5kg. Up to 18 bags per minute for 25kg and 10 bags/min on 50kg; our packing quality, and speed is unmatched'
      },
    ],
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
.v-carousel .v-window-item {
  position: absolute;
  top: 0;
  width: 100%;
  transition: 5000ms !important;
}


.intro-text {
  background-color: rgba(0, 0, 0, .15) !important;
  backdrop-filter: blur(3px);
}

.product-range {
  background-color: rgba(0, 0, 0, 0.2) !important;
}

.contact-form {
  background-color: rgba(0, 0, 0, .15) !important;
  backdrop-filter: blur(3px);
}
</style>
