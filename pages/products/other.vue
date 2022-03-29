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
            <h1 class="grey--text text--darken-2">Other Products</h1>
            <v-divider class="mt-3 mb-3"></v-divider>
            <v-card class="ma-auto" flat width="100%">
              <v-img src="/products/other-products.png" width="100%"></v-img>
            </v-card>
            <h3 class="mt-6 text-center">
              CHICK a-LICIOUS
              <v-icon class="mb-1" small>mdi-circle</v-icon>
              Sunset Braaipap
              <v-icon class="mb-1" small>mdi-circle</v-icon>
              Marogo Pap
              <v-icon class="mb-1" small>mdi-circle</v-icon>
              eendag Yellow Maize
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
  name: "OtherProducts",
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
