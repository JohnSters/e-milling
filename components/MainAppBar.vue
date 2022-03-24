<template>
  <div>
    <!--  Navigation Drawer Start  -->
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  <!--  App Bar Start  -->
    <v-app-bar class="elevation-4" :clipped-left="clipped" shaped fixed app elevate-on-scroll>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-spacer></v-spacer>
      <v-chip label color="#2E7D32" class="mr-2 font-weight-bold" dark>Contact Us: 056-515-1309</v-chip>
      <v-btn icon href="https://www.facebook.com" target="_blank">
        <v-icon color="blue" x-large>mdi-facebook</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon color="green" x-large>mdi-whatsapp</v-icon>
      </v-btn>
      <v-btn icon>
        <v-icon color="purple" x-large>mdi-instagram</v-icon>
      </v-btn>
      <v-spacer />
      <v-btn class="mr-1 font-weight-bold hidden-md-and-down" color="#F57F17" depressed rounded small outlined>
        Products
        <v-icon>mdi-script-text-outline</v-icon>
      </v-btn>
      <DropDownMenu />
      <v-btn color="#2E7D32" class="mr-1 hidden-md-and-down" dark depressed rounded small nuxt to="/">
        Documents
        <v-icon class="ml-1">mdi-folder-open-outline</v-icon>
      </v-btn>
      <v-btn color="#2E7D32" class="mr-1 hidden-md-and-down" dark depressed rounded small nuxt to="/LatestNews">
        Latest News
        <v-icon class="ml-1">mdi-book-open-outline</v-icon>
      </v-btn>
      <v-btn color="#2E7D32" class="ml-5" fab dark depressed small>
        <v-icon>mdi-face-agent</v-icon>
      </v-btn>
      <v-btn color="#2E7D32" class="ml-1" fab dark depressed small to="/">
        <v-icon>mdi-home</v-icon>
      </v-btn>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "MainAppBar",
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'e-Milling',
    }
  },
}
</script>

<style scoped>

</style>
