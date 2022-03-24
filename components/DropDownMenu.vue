<template>
  <v-menu content-class="rounded-xl mt-2 elevation-1" offset-y open-on-hover close-delay="800">
    <template v-slot:activator="{ on, attrs }">
      <v-btn
        color="#2E7D32"
        class="mr-1 hidden-md-and-down"
        dark
        depressed
        rounded
        small
        v-bind="attrs"
        v-on="on"
      >
        Company Info
        <v-icon>mdi-arrow-down</v-icon>
      </v-btn>
    </template>
    <v-list color="#2E7D32" dark>
      <v-list-item nuxt to="/info/about">
        <v-icon class="mr-2">mdi-account-details</v-icon>
        <v-list-item-title>About Us</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/profile">
        <v-icon class="mr-2">mdi-text-box</v-icon>
        <v-list-item-title>Company Profile</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/team">
        <v-icon class="mr-2">mdi-account-multiple-outline</v-icon>
        <v-list-item-title>Meet Our Team</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt>
        <v-icon class="mr-2">mdi-heart</v-icon>
        <v-list-item-title>We Care</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt>
        <v-icon class="mr-2">mdi-forest</v-icon>
        <v-list-item-title>Green Power</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt>
        <v-icon class="mr-2">mdi-package-variant-closed</v-icon>
        <v-list-item-title>Packing Excellence</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt>
        <v-icon class="mr-2">mdi-account-hard-hat</v-icon>
        <v-list-item-title>Vacancies / Jobs</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt>
        <v-icon class="mr-2">mdi-shield-search</v-icon>
        <v-list-item-title>Terms & Conditions</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  name: "DropDownMenu"
}
</script>

<style scoped>

</style>
