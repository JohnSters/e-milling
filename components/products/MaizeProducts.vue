<template>
  <v-container class="mt-4">
    <v-row>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Lucky Super Maize Meal</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link to="/products/lucky">
            <v-img src="/products/em-lucky.jpg" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Hippo Samp</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link to="/products/hippo">
            <v-img src="/products/hippo-samp.jpg" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>

      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Keyona Superior Maize Meal</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link to="/products/keyona">
            <v-img src="/products/keyona-superior.jpg" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Life Super Maize Meal</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link to="/products/life">
            <v-img src="/products/super-life-maize.jpg" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "MaizeProducts"
}
</script>

<style scoped>

</style>
