<template>
  <v-container class="mt-4">
    <v-row>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Lucky Super Maize Meal</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/em-lucky.jpg"></v-img>
          </v-card>
        </v-col>
      </v-hover>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Hippo Samp</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/hippo-samp.jpg"></v-img>
          </v-card>
        </v-col>
      </v-hover>

      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Keyona Superior Maize Meal</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/keyona-superior.jpg"></v-img>
          </v-card>
        </v-col>
      </v-hover>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Life Super Maize Meal</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/super-life-maize.jpg"></v-img>
          </v-card>
        </v-col>
      </v-hover>
    </v-row>
    <div class="mt-6 text-center"><v-btn depressed>Products Page</v-btn> - <v-btn depressed>Download Brochure <v-icon class="ml-1">mdi-download</v-icon></v-btn></div>
  </v-container>
</template>

<script>
export default {
  name: "MaizeProducts"
}
</script>

<style scoped>

</style>
