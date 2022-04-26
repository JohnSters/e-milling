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

    <div class="mt-6 mb-6 text-center hidden-sm-and-down">
      <v-btn class="orange" dark nuxt to="/products/product-main">Product List</v-btn>
      -
      <v-btn href="/downloads/eendag-meule-broshure.pdf" download="" depressed>Download Brochure
        <v-icon class="ml-1">mdi-download</v-icon>
      </v-btn>
    </div>
    <div class="mt-2 ml-6 hidden-md-and-up">
      <v-btn depressed rounded small>Products Page</v-btn>
      <v-btn href="/downloads/eendag-meule-broshure.pdf" download="" class="mt-2" depressed rounded small>Download Brochure
        <v-icon class="ml-1">mdi-download</v-icon>
      </v-btn>
    </div>
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
