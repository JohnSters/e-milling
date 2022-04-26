<template>
  <div>
    <template>
      <v-parallax height="300" src="/office-inside.jpg"></v-parallax>
    </template>
    <v-container class="care">
    <v-card elevation="6" shaped>
      <v-container>
        <h1 class="grey--text text--darken-2">We Care About Our Communities</h1>
        <v-divider class="mt-2 mb-2"></v-divider>
        <p class="grey--text text--darken-2">Where possible, we support small enterprises by providing them with competitive pricing. We assist various schools and feeding schemes in order to provide for our children and our future. We support different welfare organisations with monthly maize meal donations in order to help feed the less fortunate.</p>
        <p class="grey--text text--darken-2">We care about a fit and healthy community. Recently we became the proud sponsor of Bothaville Marathon-club.</p>
        <p class="grey--text text--darken-2">We strive to appoint the best qualified personnel for every position within the company. We aim to uplift currently employed personnel through training and skills development.  Our current workforce is approximately 118 employees. </p>
        <v-row>
          <v-col
            cols="12"
            sm="6"
            md="4"
          >
            <v-card
              class="pa-2"
              tile
            >
              <v-img src="/wecare6.jpg" max-width="355"></v-img>
            </v-card>
          </v-col>
          <v-col
            cols="6"
            md="4"
          >
            <v-card class="d-flex align-center justify-center" flat  min-height="250">
              Eendag Meule is the proud sponsor of Bothaville Marathonklub.
            </v-card>
          </v-col>
        </v-row>
        <v-row>
          <v-col
            cols="12"
            sm="6"
            md="4"
          >
            <v-card
              class="pa-2"
              tile
            >
              <v-img src="/wecare5.jpg" max-width="355"></v-img>
            </v-card>
          </v-col>
          <v-col
            cols="6"
            md="4"
          >
            <v-card class="d-flex align-center justify-center" flat  min-height="250">
              After a long year’s work we celebrate with a festive braai and year-end party.
            </v-card>
          </v-col>
        </v-row>
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
  name: "WeCare"
}
</script>

<style scoped>
.care {
  margin-top: -150px;
}
</style>
