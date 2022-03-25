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
            <v-list-item-title v-text="item.title"/>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!--  App Bar Start  -->
    <v-app-bar height="75vh" class="elevation-4" :clipped-left="clipped" shaped fixed app elevate-on-scroll>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"/>
      <v-tooltip bottom color="blue">
        <template #activator="{ on, attrs }">
          <v-btn
            color="blue"
            class="ml-5 elevation-2"
            v-bind="attrs"
            nuxt
            to="/"
            dark
            v-on="on"
          >
            <v-icon>mdi-home</v-icon>
          </v-btn>
        </template>
        <span>Home Page</span>
      </v-tooltip>
      <ContactInfo />
      <v-spacer></v-spacer>
      <v-hover v-slot="{ hover }" close-delay="500">
        <v-btn class="font-weight-bold mr-1 hidden-md-and-down" color="#FFB300" :elevation="hover ? 3 : 0" :class="{ 'on-hover': hover }" depressed outlined>
          Products
          <v-icon>mdi-script-text-outline</v-icon>
        </v-btn>
      </v-hover>
      <DropDownMenu/>
      <v-btn class="mr-1 font-weight-bold green--text hidden-md-and-down" text nuxt>
        Documents
        <v-icon class="ml-1">mdi-folder-open-outline</v-icon>
      </v-btn>
      <v-btn class="font-weight-bold green--text hidden-md-and-down" text nuxt>
        Latest News
        <v-icon class="ml-1">mdi-book-open-outline</v-icon>
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
      menuValue: false,
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

<style lang="scss" scoped>
.v-btn.active .v-icon {
  animation: shake 0.5s;
  animation-iteration-count: infinite;
}

@keyframes shake {
  0% { transform: translate(1px, 1px) rotate(0deg); }
  10% { transform: translate(-1px, -2px) rotate(-1deg); }
  20% { transform: translate(-3px, 0px) rotate(1deg); }
  30% { transform: translate(3px, 2px) rotate(0deg); }
  40% { transform: translate(1px, -1px) rotate(1deg); }
  50% { transform: translate(-1px, 2px) rotate(-1deg); }
  60% { transform: translate(-3px, 1px) rotate(0deg); }
  70% { transform: translate(3px, 1px) rotate(-1deg); }
  80% { transform: translate(-1px, -1px) rotate(1deg); }
  90% { transform: translate(1px, 2px) rotate(0deg); }
  100% { transform: translate(1px, -2px) rotate(-1deg); }
}
</style>
