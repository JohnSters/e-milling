<template>
  <v-container>
    <v-row>
      <v-col
        cols="12"
        lg="6"
      >
        <v-card
          class="pa-2"
          flat
          tile
        >
          <v-card
            :loading="loading"
            class="mx-auto my-12"
            max-width="374"
          >
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-card-title>Contact Info</v-card-title>

            <v-card-text>
              <div class="my-4 text-subtitle-1">
                Eendag Meule Bothaville (Pty) Ltd
                <br>
                14 – 16 First Avenue, Industria
                <br>
                Bothaville, 9660
              </div>

              <div>Tel: 056 515 1309 <v-icon small>mdi-phone</v-icon> </div>
            </v-card-text>

            <v-divider class="mx-4"></v-divider>

            <v-card-text>
              <v-chip-group
                v-model="selection"
                active-class="deep-purple accent-4 white--text"
                column
              >
                <v-chip>
                  <v-icon left>
                    mdi-email
                  </v-icon>
                  pa@emilling.co.za
                </v-chip>

              </v-chip-group>
            </v-card-text>
          </v-card>
        </v-card>
      </v-col>
      <v-col
        cols="12"
        lg="6"
      >
        <v-card
          class="pa-2"
          flat
          tile
        >
          <v-card
            :loading="loading"
            class="mx-auto my-12"
            max-width="374"
          >
            <template slot="progress">
              <v-progress-linear
                color="deep-purple"
                height="10"
                indeterminate
              ></v-progress-linear>
            </template>

            <v-card-title>Office Hours</v-card-title>

            <v-card-text>
              <div class="my-4 text-subtitle-1">
                Monday to Friday
                <br>
                7:30 - 16:30
              </div>

              <div>Closed on weekends and public holidays</div>
            </v-card-text>
          </v-card>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "contact-us"
}
</script>

<style scoped>

</style>
