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
      <!-- -->

      <v-list nav dense>
        <div v-for="(link, i) in links" :key="i">

          <v-list-item
            v-if="!link.subLinks"
            :to="link.to"
            class="v-list-item"
          >
            <v-list-item-icon>
              <v-icon>{{ link.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-title v-text="link.text" />
          </v-list-item>

          <v-list-group
            v-else
            :key="link.text"
            no-action
            :prepend-icon="link.icon"
            :value="false"
          >
            <template v-slot:activator>
              <v-list-item-title>{{ link.text }}</v-list-item-title>
            </template>

            <v-list-item
              v-for="(sublink) in link.subLinks"
              :to="sublink.to"
              :key="sublink.text"
            >
              <v-list-item-icon>
                <v-icon>{{ sublink.icon }}</v-icon>
              </v-list-item-icon>
              <v-list-item-title>{{ sublink.text }}</v-list-item-title>
            </v-list-item>
          </v-list-group>
        </div>
      </v-list>

    </v-navigation-drawer>
    <!--  App Bar Start  -->
    <v-app-bar height="75vh" class="elevation-4" :clipped-left="clipped" shaped fixed app elevate-on-scroll>
      <v-app-bar-nav-icon class="hidden-md-and-up" @click.stop="drawer = !drawer"/>
      <v-tooltip bottom>
        <template #activator="{ on, attrs }">
          <v-btn
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
      <ContactInfo/>
      <v-spacer></v-spacer>
      <ProductDropdown />
      <v-btn class="font-weight-bold hidden-sm-and-down" color="#148a5c" text nuxt to="/latest-news">
        Latest News
        <v-icon class="ml-1">mdi-book-open-outline</v-icon>
      </v-btn>
      <InfoDropdown />
      <v-btn class="mr-1 font-weight-bold hidden-sm-and-down sm12" color="#148a5c" text nuxt>
        Documents
        <v-icon class="ml-1">mdi-folder-open-outline</v-icon>
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
      links: [
        {
          to     : '/',
          icon   : 'mdi-home',
          text   : 'Home',
        },
        {
          icon     : 'mdi-folder',
          text     : 'Products',
          subLinks : [
            {
              text : 'Lucky Super Maize Meal',
              to    : '/templates',
              icon  : 'mdi-view-list'
            },
            {
              text : 'New Template',
              to    : '/templates/new',
              icon  : 'mdi-plus'
            },
          ]
        },
        {
          icon     : 'mdi-application',
          text     : 'Applications',
          subLinks : [
            {
              text : 'View Applications',
              to    : '/apps',
              icon  : 'mdi-view-list'
            },
            {
              text : 'New Application',
              to    : '/apps',
              icon  : 'mdi-plus'
            },
          ]
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

.v-application--is-ltr .v-list--dense.v-list--nav .v-list-group--no-action > .v-list-group__items > .v-list-item {
  padding: 0 8px;
}

@keyframes shake {
  0% {
    transform: translate(1px, 1px) rotate(0deg);
  }
  10% {
    transform: translate(-1px, -2px) rotate(-1deg);
  }
  20% {
    transform: translate(-3px, 0px) rotate(1deg);
  }
  30% {
    transform: translate(3px, 2px) rotate(0deg);
  }
  40% {
    transform: translate(1px, -1px) rotate(1deg);
  }
  50% {
    transform: translate(-1px, 2px) rotate(-1deg);
  }
  60% {
    transform: translate(-3px, 1px) rotate(0deg);
  }
  70% {
    transform: translate(3px, 1px) rotate(-1deg);
  }
  80% {
    transform: translate(-1px, -1px) rotate(1deg);
  }
  90% {
    transform: translate(1px, 2px) rotate(0deg);
  }
  100% {
    transform: translate(1px, -2px) rotate(-1deg);
  }
}
</style>
