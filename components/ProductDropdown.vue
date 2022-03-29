<template>
  <v-menu
    v-model="menuValue"
    content-class="mt-2 elevation-3 rounded-xl"
    offset-y
    open-on-hover
    close-delay="800"
  >
    <template v-slot:activator="{ on, attrs }">
      <v-btn
        class="mr-3 hidden-md-and-down font-weight-bold rounded-xl"
        color="#148a5c"
        dark
        large
        v-bind="attrs"
        :class="{active: menuValue}"
        v-on="on"
      >
        Product Range
        <v-icon>mdi-arrow-up</v-icon>
      </v-btn>
    </template>
    <v-list color="darkgreen" dark>
      <v-list-item nuxt to="/products/lucky">
        <v-icon class="mr-2" small>mdi-circle</v-icon>
        <v-list-item-title>Lucky Super Maize Meal</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/products/life">
        <v-icon class="mr-2" small>mdi-circle</v-icon>
        <v-list-item-title>Life Super Maize Meal</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/products/keyona">
        <v-icon class="mr-2" small>mdi-circle</v-icon>
        <v-list-item-title>Keyona Superior - Special Maize Meal</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/products/hippo">
        <v-icon class="mr-2" small>mdi-circle</v-icon>
        <v-list-item-title>Hippo Samp</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/products/other">
        <v-icon class="mr-2" small>mdi-circle</v-icon>
        <v-list-item-title>Other Products</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/products/plaasjapie">
        <v-icon class="mr-2" small>mdi-circle</v-icon>
        <v-list-item-title>Niche Products - Plaasjapie</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  name: "ProductDropdown",
  data() {
    return {
      menuValue: false,
    }
  }
}
</script>

<style scoped>
.v-btn.active .v-icon {
  transform: rotate(180deg);
}
</style>
