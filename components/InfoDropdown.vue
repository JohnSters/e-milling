<template>
  <v-menu
    v-model="menuValue"
    content-class="rounded-xl mt-2 elevation-1"
    offset-y
    open-on-hover
    close-delay="800"
    nudge-left="25"
  >
    <template v-slot:activator="{ on, attrs }">
      <v-btn
        class="mr-2 hidden-sm-and-down font-weight-bold rounded-xl"
        color="#148a5c"
        v-bind="attrs"
        text
        :class="{active: menuValue}"
        v-on="on"
      >
        Company Info
        <v-icon>mdi-arrow-up</v-icon>
      </v-btn>
    </template>
    <v-list color="#148a5c" dark>
      <v-list-item nuxt to="/info/about-us">
        <v-icon class="mr-2">mdi-account-details</v-icon>
        <v-list-item-title>About Us</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/company-profile">
        <v-icon class="mr-2">mdi-text-box</v-icon>
        <v-list-item-title>Company Profile</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/our-team">
        <v-icon class="mr-2">mdi-account-multiple-outline</v-icon>
        <v-list-item-title>Meet Our Team</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/we-care">
        <v-icon class="mr-2">mdi-heart</v-icon>
        <v-list-item-title>We Care</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/green-power">
        <v-icon class="mr-2">mdi-forest</v-icon>
        <v-list-item-title>Green Power</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/packing-excellence">
        <v-icon class="mr-2">mdi-package-variant-closed</v-icon>
        <v-list-item-title>Packing Excellence</v-list-item-title>
      </v-list-item>
      <v-list-item to="/info/vacancies" nuxt>
        <v-icon class="mr-2">mdi-account-hard-hat</v-icon>
        <v-list-item-title>Vacancies / Jobs</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/terms-conditions">
        <v-icon class="mr-2">mdi-shield-search</v-icon>
        <v-list-item-title>Terms & Conditions</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  name: "InfoDropdown",
  data() {
    return {
      menuValue: null
    };
  }
}
</script>

<style lang="scss" scoped>
.v-btn.active .v-icon {
  transform: rotate(180deg);
}
</style>
