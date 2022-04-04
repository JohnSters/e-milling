<template>
  <v-card>
    <v-footer
      v-bind="localAttrs"
      :padless="padLess"
    >
      <v-card
        flat
        tile
        width="100%"
        class="midnight text-center"
        color="darkgreen"
      >
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4"
            icon
          >
            <v-icon size="24px">
              {{ icon }}
            </v-icon>
          </v-btn>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-text class="white--text">
          {{ new Date().getFullYear() }} — <strong>©Eendag Meule Bothaville (Pty) Ltd. All rights reserved.</strong>
          <br>
          <h3>Tel: 056-515-1309</h3>
        </v-card-text>
      </v-card>
    </v-footer>
  </v-card>
</template>

<script>
export default {

  name: 'bottom-footer',
  data: () => ({
    icons: [
      'mdi-facebook',
      'mdi-whatsapp',
      'mdi-instagram',
      'mdi-linkedin',
    ],
    items: [
      'default',
      'absolute',
      'fixed',
    ],
    padLess: true,
    variant: 'default',
  }),
  mounted() {
    const theme = localStorage.getItem("useDarkTheme");
    if (theme) {
      if (theme === "true") {
        this.$vuetify.theme.dark = true;
      } else this.$vuetify.theme.dark = false;
    }
  },
  methods: {
    toggleTheme() {
      this.$vuetify.theme.dark=!this.$vuetify.theme.dark;
      localStorage.setItem("useDarkTheme", this.$vuetify.theme.dark.toString())
    }
  },
  computed: {
    localAttrs () {
      const attrs = {}

      if (this.variant === 'default') {
        attrs.absolute = false
        attrs.fixed = false
      } else {
        attrs[this.variant] = true
      }
      return attrs
    },
  },
}
</script>

<style scoped>

</style>
