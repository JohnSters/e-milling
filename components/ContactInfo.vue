<template>
  <v-dialog max-width="600">
    <template #activator="{ on: dialog }">
      <v-tooltip v-model="menuValue" bottom color="green">
        <template #activator="{ on: tooltip, attrs }">
          <v-btn
            color="green"
            class="ml-2 elevation-2"
            v-bind="attrs"
            dark
            :class="{hover: menuValue}"
            v-on="{ ...tooltip, ...dialog }"
          >
            <v-icon>mdi-phone</v-icon>
          </v-btn>
        </template>
        <span>Get in Touch</span>
      </v-tooltip>
    </template>
    <template v-slot:default="dialog">
      <v-card>
        <v-toolbar
          color="green"
          dark
        ><h2 class="ma-auto">Contact Us</h2></v-toolbar>
        <v-container>
          <v-card flat>
            <h3>Contact Info</h3>
            <div>
              Eendag Meule Bothaville (Pty) Ltd
              <br>
              14 – 16 First Avenue, Industria
              <br>
              Bothaville, 9660
              <v-divider class="mt-2 mb-2"></v-divider>
              Tel: 056-515-1309 <v-icon class="mb-1" small>mdi-phone</v-icon> / Email: pa@emilling.co.za
              <v-divider class="mt-2 mb-2"></v-divider>
              <h3>Office Hours</h3>
              <div>
                Monday to Friday
                from: 7:30 - 16:30
                <br>
                Closed on weekends and public holidays
                <v-divider class="mt-2 mb-2"></v-divider>
                <v-btn class="rounded-xl mt-3" depressed href="https://goo.gl/maps/8rijZaZbutDWf4nF8" target="_blank">Find us on Google Maps</v-btn>
              </div>
            </div>
          </v-card>
        </v-container>
        <v-card-actions class="justify-end">
          <v-btn
            text
            small
            class="rounded-xl"
            @click="dialog.value = false"
          >Close</v-btn>
        </v-card-actions>
      </v-card>
    </template>
  </v-dialog>
</template>

<script>
export default {
  name: "ContactInfo",
  data() {
    return {
      menuValue: null,
    }
  }
}
</script>

<style lang="scss" scoped>
.v-btn:hover .v-icon {
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
