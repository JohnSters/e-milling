<template>
  <!-- Home page product category. Imports several other components /components/products -->
  <v-container class="mt-6">
    <v-tabs centered color="darkgreen">
      <v-tab>
        Maize Range
      </v-tab>
      <v-tab>
        Animal Feeds
      </v-tab>
      <v-tab>
        Nichè Products
      </v-tab>
      <!--      -->
      <!-- Maize products category component -->
      <v-tab-item>
        <MaizeProducts />
      </v-tab-item>
      <!-- END -->

      <!--  Animal Feeds category component  -->
      <v-tab-item>
        <FeedProducts />
      </v-tab-item>
      <!--  END  -->

      <!-- Niche products category component -->
      <v-tab-item>
        <NicheProducts />
      </v-tab-item>
      <!-- END -->

    </v-tabs>
  </v-container>
</template>

<script>
import MaizeProducts from "~/components/products/MaizeProducts";
import NicheProducts from "~/components/products/NicheProducts";
import FeedProducts from "~/components/products/FeedProducts";
export default {
name: "ProductCategory",
  components: {FeedProducts, NicheProducts, MaizeProducts}
}
</script>

<style scoped>

</style>
