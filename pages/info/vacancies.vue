<template>
  <div>
    <template>
      <v-parallax height="300" src="/office-inside.jpg"></v-parallax>
    </template>
    <v-container class="care">
      <v-card elevation="6" shaped>
        <v-container>
          <h1 class="grey--text text--darken-2">Vacancies / Jobs Available</h1>
          <v-divider class="mt-2 mb-2"></v-divider>
          <h1 class="grey--text text--darken-2 font-weight-light text-center">There are no vacancies available at this time.
            <br>
            Please watch this space for more information.</h1>
        </v-container>
      </v-card>
    </v-container>
    <div class="mt-12">
      <ProductCategory />
    </div>
  </div>
</template>

<script>
export default {
  name: "JobsAvailable",
}
</script>

<style scoped>
.care {
  margin-top: -150px;
}
</style>
