<template>
  <v-container class="mt-6">
      <v-tabs right>
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
          <v-row>
            <v-hover v-slot="{ hover }">
              <v-col
                cols="12"
                md="4"
              >
                <p class="text-center">Super Maize Meal 50kg</p>
                <v-card class="pa-6 ml-6" :elevation="hover ? 6 : 2" link>
                  <v-img src="products/image1.jpg"></v-img>
                </v-card>
              </v-col>
            </v-hover>
            <v-hover v-slot="{ hover }">
            <v-col
              cols="12"
              md="4"
            >
              <p class="text-center">Super Maize Meal 50kg</p>
              <v-card class="pa-6 ma-3" :elevation="hover ? 4 : 2" link>
                <v-img src="products/image3.jpg"></v-img>
              </v-card>
            </v-col>
          </v-hover>
            <v-hover v-slot="{ hover }">
              <v-col
                cols="12"
                md="4"
              >
                <p class="text-center">Super Maize Meal 50kg</p>
                <v-card class="pa-6 mr-6" :elevation="hover ? 12 : 2" link>
                  <v-img src="products/image4.jpg"></v-img>
                </v-card>
              </v-col>
            </v-hover>
            <v-hover v-slot="{ hover }">
              <v-col
                cols="12"
                md="4"
              >
                <p class="text-center">Super Maize Meal 50kg</p>
                <v-card class="pa-6 ml-6" :elevation="hover ? 12 : 2" link>
                  <v-img src="products/image4.jpg"></v-img>
                </v-card>
              </v-col>
            </v-hover>
            <v-hover v-slot="{ hover }">
              <v-col
                cols="12"
                md="4"
              >
                <p class="text-center">Super Maize Meal 50kg</p>
                <v-card class="pa-6 ma-3" :elevation="hover ? 6 : 2" link>
                  <v-img src="products/image5.jpg"></v-img>
                </v-card>
              </v-col>
            </v-hover>
            <v-hover v-slot="{ hover }">
              <v-col
                cols="12"
                md="4"
              >
                <p class="text-center">Super Maize Meal 50kg</p>
                <v-card class="pa-6 mr-6" :elevation="hover ? 6 : 2" link>
                  <v-img src="products/image6.jpg"></v-img>
                </v-card>
              </v-col>
            </v-hover>
            <v-hover v-slot="{ hover }">
              <v-col
                cols="12"
                md="4"
              >
                <p class="text-center">Super Maize Meal 50kg</p>
                <v-card class="pa-6 ml-6" :elevation="hover ? 6 : 2" link>
                  <v-img src="products/image7.jpg"></v-img>
                </v-card>
              </v-col>
            </v-hover>
            <v-hover v-slot="{ hover }">
              <v-col
                cols="12"
                md="4"
              >
                <p class="text-center">Super Maize Meal 50kg</p>
                <v-card class="pa-6 ma-3" :elevation="hover ? 6 : 2" link>
                  <v-img src="products/image8.jpg"></v-img>
                </v-card>
              </v-col>
            </v-hover>
            <v-hover v-slot="{ hover }">
              <v-col
                cols="12"
                md="4"
              >
                <p class="text-center">Super Maize Meal 50kg</p>
                <v-card class="pa-6 mr-6" :elevation="hover ? 6 : 2" link>
                  <v-img src="products/image9.jpg"></v-img>
                </v-card>
              </v-col>
            </v-hover>
          </v-row>
        </v-tab-item>
        <v-tab-item>
          <v-card flat>
            <v-card-text>
              <p>
                Morbi nec metus. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis tellus, vitae iaculis lacus elit id tortor. Sed mollis, eros et ultrices tempus, mauris ipsum aliquam libero, non adipiscing dolor urna a orci. Curabitur ligula sapien, tincidunt non, euismod vitae, posuere imperdiet, leo. Nunc sed turpis.
              </p>

              <p>
                Suspendisse feugiat. Suspendisse faucibus, nunc et pellentesque egestas, lacus ante convallis tellus, vitae iaculis lacus elit id tortor. Proin viverra, ligula sit amet ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In hac habitasse platea dictumst. Fusce ac felis sit amet ligula pharetra condimentum.
              </p>

              <p>
                Sed consequat, leo eget bibendum sodales, augue velit cursus nunc, quis gravida magna mi a libero. Nam commodo suscipit quam. In consectetuer turpis ut velit. Sed cursus turpis vitae tortor. Aliquam eu nunc.
              </p>

              <p>
                Etiam ut purus mattis mauris sodales aliquam. Ut varius tincidunt libero. Aenean viverra rhoncus pede. Duis leo. Fusce fermentum odio nec arcu.
              </p>

              <p class="mb-0">
                Donec venenatis vulputate lorem. Aenean viverra rhoncus pede. In dui magna, posuere eget, vestibulum et, tempor auctor, justo. Fusce commodo aliquam arcu. Suspendisse enim turpis, dictum sed, iaculis a, condimentum nec, nisi.
              </p>
            </v-card-text>
          </v-card>
        </v-tab-item>
        <v-tab-item>
          <v-card flat>
            <v-card-text>
              <p>
                Fusce a quam. Phasellus nec sem in justo pellentesque facilisis. Nam eget dui. Proin viverra, ligula sit amet ultrices semper, ligula arcu tristique sapien, a accumsan nisi mauris ac eros. In dui magna, posuere eget, vestibulum et, tempor auctor, justo.
              </p>

              <p class="mb-0">
                Cras sagittis. Phasellus nec sem in justo pellentesque facilisis. Proin sapien ipsum, porta a, auctor quis, euismod ut, mi. Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nam at tortor in tellus interdum sagittis.
              </p>
            </v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs>
  </v-container>
</template>

<script>
export default {
  name: "CatagoryMain",
  data() {
    return {

    }
  }
}
</script>

<style scoped>

</style>
