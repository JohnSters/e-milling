<template>
  <!--
    The default page will be displayed on every created page if it does not have a specified default.
    Use this page if you want to display products on all pages.
   -->
  <v-app dark>
    <MainAppBar />
    <v-main>
        <Nuxt />
    </v-main>

    <FooterMain />
    <div>
      <SocialChat
        icon
        id="social-button"
        :attendants="attendants"
      >
        <p slot="header" >Chat to us on whatsapp for any question, or sales related topics.</p>
        <template v-slot:button>
          <img
            src="https://raw.githubusercontent.com/ktquez/vue-social-chat/master/src/icons/whatsapp.svg"
            alt="icon whatsapp"
            aria-hidden="true"
          >
        </template>
        <small slot="footer">Opening hours: 8am to 6pm</small>
      </SocialChat>
    </div>
  </v-app>
</template>

<script>
import { SocialChat } from 'vue-social-chat'

export default {
  name: 'DefaultLayout',
  components: {
    SocialChat
  },
  data() {
    return {
      attendants: [
        {
          app: 'whatsapp',
          label: 'Sales',
          name: 'Belinda Botha',
          number: '+27832568151',
          avatar: {
            src: '/Belinda Botha.jpg',
            alt: 'Sales'
          }
        },
        // ...
      ],
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
    }
  },
}
</script>

<style>

:root #social-button {
  --vsc-bg-header: green;
  --vsc-bg-footer: #fafafa;
  --vsc-text-color-header: white;
  --vsc-text-color-footer: green;
  --vsc-bg-button: green;
  --vsc-text-color-button: purple;
  --vsc-outline-color: darkgreen;
  --vsc-border-color-bottom-header: teal;
  --vsc-border-color-top-footer: #f3f3f3;
}

.container {
  max-width: 1200px;
}
</style>
