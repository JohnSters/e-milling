<template>
  <v-container class="mt-4">
  <v-row>
    <v-hover v-slot="{ hover }">
      <v-col
        cols="12"
        md="3"
      >
        <p class="text-center">Plaasjapie Growwe Braaipap</p>
        <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
          <v-img src="/products/niche1.png" height="360"></v-img>
        </v-card>
      </v-col>
    </v-hover>
    <v-hover v-slot="{ hover }">
      <v-col
        cols="12"
        md="3"
      >
        <p class="text-center">Plaasjapie Bittergrowwe Braaipap</p>
        <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
          <v-img src="/products/niche2.png" height="360"></v-img>
        </v-card>
      </v-col>
    </v-hover>

    <v-hover v-slot="{ hover }">
      <v-col
        cols="12"
        md="3"
      >
        <p class="text-center">Plaasjapie Semelverrykte Braaipap</p>
        <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
          <v-img src="/products/niche3.png" height="360"></v-img>
        </v-card>
      </v-col>
    </v-hover>
    <v-hover v-slot="{ hover }">
      <v-col
        cols="12"
        md="3"
      >
        <p class="text-center">Plaasjapie Growwe Geelmeel</p>
        <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
          <v-img src="/products/niche4.png" height="360"></v-img>
        </v-card>
      </v-col>
    </v-hover>
  </v-row>
  </v-container>
</template>

<script>
export default {
  name: "NicheProducts"
}
</script>

<style scoped>

</style>
