<template>
  <div>
    <template>
      <v-parallax height="300" src="/office-inside.jpg"></v-parallax>
    </template>
    <v-container class="team">
      <v-card elevation="6" shaped>
        <v-container>
          <h1>Meet our Team</h1>
          <v-divider class="mt-2 mb-2"></v-divider>
          <v-row>
            <v-col
              cols="12"
              sm="4"
            >
              <v-card
                class="mx-auto"
                max-width="344"
              >
                <v-img src="/team/hannalie.jpg" height="390"></v-img>

                <v-card-title>
                  Hannalie Hayes
                </v-card-title>

                <v-card-subtitle>
                  CEO
                </v-card-subtitle>

                <v-card-subtitle>
                  Contact: 083-380-6211 / <v-icon class="mb-1" small>mdi-cellphone</v-icon>
                </v-card-subtitle>
              </v-card>
            </v-col>

            <v-col
              cols="12"
              sm="4"
            >
              <v-card
                class="mx-auto rounded-br-xl"
                max-width="344"
              >
                <v-img src="/team/karen.jpg" height="390"></v-img>

                <v-card-title>
                  Karen Kock
                </v-card-title>

                <v-card-subtitle>
                  Financial Manager
                </v-card-subtitle>

                <v-card-subtitle>
                  Contact: Number Needed / <v-icon class="mb-1" small>mdi-cellphone</v-icon>
                </v-card-subtitle>

              </v-card>
            </v-col>

            <v-col
              cols="12"
              sm="4"
            >
              <v-card
                class="mx-auto"
                max-width="344"
              >
                <v-img src="/team/martin.jpeg" height="390"></v-img>

                <v-card-title>
                  Martin van Deventer
                </v-card-title>

                <v-card-subtitle>
                  Executive Director
                </v-card-subtitle>

                <v-card-subtitle>
                  Contact: 083 447 6156 / <v-icon class="mb-1" small>mdi-cellphone</v-icon>
                </v-card-subtitle>

              </v-card>
            </v-col>
            <v-col
              cols="12"
              sm="4"
            >
              <v-card
                class="mx-auto"
                max-width="344"
              >
                <v-img src="/team/kobie.jpg" height="390"></v-img>

                <v-card-title>
                  Kobie Burger
                </v-card-title>

                <v-card-subtitle>
                  Marketing Manager
                </v-card-subtitle>

                <v-card-subtitle>
                  Contact: 084 310 9678 / <v-icon class="mb-1" small>mdi-cellphone</v-icon>
                </v-card-subtitle>

              </v-card>
            </v-col>

            <v-col
              cols="12"
              sm="4"
            >
              <v-card
                class="mx-auto"
                max-width="344"
              >
                <v-img src="/team/david.jpg" height="390"></v-img>

                <v-card-title>
                  David Van Niekerk
                </v-card-title>

                <v-card-subtitle>
                  Packaging & Shipping Manager
                </v-card-subtitle>

                <v-card-subtitle>
                  Contact: 056-515-3908 / <v-icon class="mb-1" small>mdi-phone</v-icon>
                </v-card-subtitle>

              </v-card>
            </v-col>

            <v-col
              cols="12"
              sm="4"
            >
              <v-card
                class="mx-auto"
                max-width="344"
              >
                <v-img src="/team/george.jpg" height="390"></v-img>

                <v-card-title>
                  George Hayes
                </v-card-title>

                <v-card-subtitle>
                  Production Manager
                </v-card-subtitle>

                <v-card-subtitle>
                  Contact: 056-515-3908 / <v-icon class="mb-1" small>mdi-phone</v-icon>
                </v-card-subtitle>

              </v-card>
            </v-col>

          </v-row>
        </v-container>
      </v-card>
    </v-container>
    <div class="mt-12">
      <ProductCategory />
    </div>
  </div>
</template>

<script>
export default {
  name: "meet-our-team"
}
</script>

<style scoped>
.team {
  margin-top: -150px;
}
</style>
