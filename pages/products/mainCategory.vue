<template>
  <v-container class="mt-6">
    <v-tabs centered>
      <v-tab>
        Niche Products
      </v-tab>
      <v-tab>
        Maize Range
      </v-tab>
      <v-tab>
        Animal Feeds
      </v-tab>

      <v-tab-item class="mt-2">
        Niche Products
      </v-tab-item>
      <v-tab-item>
        <maize-products />
      </v-tab-item>
      <v-tab-item>
        Animal Feeds
      </v-tab-item>
    </v-tabs>
  </v-container>
</template>

<script>
import MaizeProducts from "~/components/products/MaizeProducts";
export default {
name: "MainCategory",
  components: {MaizeProducts}
}
</script>

<style scoped>

</style>
