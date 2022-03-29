<template>
  <div>
    <template>
      <v-parallax height="300" src="/machinery6.jpg"></v-parallax>
    </template>
    <v-container class="about">
      <v-row>
        <v-card
          elevation="6"
          shaped
          width="100%"
        >
          <v-container>
            <h1 class="grey--text text--darken-2">Nichè Products - Plaasjapie assorted Braaipap range</h1>
            <v-divider class="mt-3 mb-3"></v-divider>
            <v-card class="ma-auto" flat width="100%">
              <v-img src="/products/plaasjapie.png" width="100%"></v-img>
            </v-card>
            <h3 class="mt-6 text-center">
              Our niche products that are available at selected stores such as e.g. road stalls
              Unique feature of our plaasjapie braaipap is that the design is changed
              regularly. The product is packed in a linen bag, that is often use
              of needle work and quilting.
            </h3>
          </v-container>
        </v-card>
      </v-row>
    </v-container>
    <ProductCategory/>
  </div>
</template>

<script>
export default {
  name: "PlaasJapieProducts",
  data() {
    return {
      search: '',
      dialog: false,
    }
  },
}
</script>

<style scoped>
.container {
}

.about {
  margin-top: -150px;
}
</style>
