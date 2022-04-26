<template>
  <div>
    <template>
      <v-parallax height="300" src="/our-team.jpg"></v-parallax>
    </template>
    <v-container class="team">
      <v-card elevation="6" shaped>
        <v-container>
          <v-tabs centered color="darkgreen">
          <v-tab>
            Management Team
          </v-tab>
          <v-tab>
            Sales Team
          </v-tab>
          <!--      -->
          <!-- Maize products category component -->
          <v-tab-item class="mt-6 mb-6">
            <ManagementTeam />
          </v-tab-item>
          <!-- END -->

          <!--  Animal Feeds category component  -->
          <v-tab-item class="mt-6 mb-6">
            <SalesTeam />
          </v-tab-item>
          <!--  END  -->


          </v-tabs>
        </v-container>

      </v-card>

      <div class="mt-16 mb-6 text-center hidden-sm-and-down">
        <v-btn depressed nuxt to="/products/product-main">Products Page</v-btn>
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
  </div>
</template>

<script>
import ManagementTeam from "~/pages/info/management-team";
import SalesTeam from "~/pages/info/sales-team";
export default {
  name: "OurTeam",
  components: {SalesTeam, ManagementTeam},
}
</script>

<style scoped>
.team {
  margin-top: -150px;
}
</style>
