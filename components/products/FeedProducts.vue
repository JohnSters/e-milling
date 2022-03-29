<template>
  <v-container class="mt-4">
  <v-row>
    <v-hover v-slot="{ hover }">
      <v-col
        cols="12"
        md="3"
      >
        <p class="text-center">Eendag Yellow Maize</p>
        <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
          <v-img src="/products/yellow.jpg" height="360"></v-img>
        </v-card>
      </v-col>
    </v-hover>
    <v-hover v-slot="{ hover }">
      <v-col
        cols="12"
        md="3"
      >
        <p class="text-center">Chick a-Licious</p>
        <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
          <v-img src="/products/chick.jpg" height="360"></v-img>
        </v-card>
      </v-col>
    </v-hover>
  </v-row>
  <div class="mt-6 text-center"><v-btn depressed>Products Page</v-btn> - <v-btn depressed>Download Brochure <v-icon class="ml-1">mdi-download</v-icon></v-btn></div>
  </v-container>
</template>

<script>
export default {
  name: "FeedProducts"
}
</script>

<style scoped>

</style>
