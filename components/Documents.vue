<template>
  <v-menu
    v-model="menuValue"
    content-class="rounded-xl mt-2 elevation-1"
    offset-y
    open-on-hover
    close-delay="800"
  >
    <template v-slot:activator="{ on, attrs }">
      <v-btn
        class="ml-2 hidden-sm-and-down font-weight-bold"
        color="#148a5c"
        depressed
        dark
        v-bind="attrs"
        :class="{active: menuValue}"
        v-on="on"
      >
        Documents
        <v-icon>mdi-arrow-up</v-icon>
      </v-btn>
    </template>
    <v-list color="#148a5c" dark>
      <h3 class="ml-5">Admin</h3>
      <v-divider class="ma-3"></v-divider>
      <v-list-item nuxt to="/info/about-us">
        <v-icon class="mr-2">mdi-download</v-icon>
        <v-list-item-title>EENDAG MEULE Credit Application Form.pdf</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/company-profile">
        <v-icon class="mr-2">mdi-download</v-icon>
        <v-list-item-title>DS Generic Credit Policy and SLA Eendagmeule Draft1.pdf</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/our-team">
        <v-icon class="mr-2">mdi-download</v-icon>
        <v-list-item-title>Kontantaansoek 2018.pdf</v-list-item-title>
      </v-list-item>
      <h3 class="ml-5 mt-5">Certification</h3>
      <v-divider class="ma-3"></v-divider>
      <v-list-item nuxt to="/info/we-care">
        <v-icon class="mr-2">mdi-download</v-icon>
        <v-list-item-title>Halaal</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt to="/info/green-power">
        <v-icon class="mr-2">mdi-download</v-icon>
        <v-list-item-title>Food Safety.pdf</v-list-item-title>
      </v-list-item>
      <v-list-item nuxt>
        <v-icon class="mr-2">mdi-download</v-icon>
        <v-list-item-title>HACCP.pdf</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  name: "CompanyDocuments",
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
