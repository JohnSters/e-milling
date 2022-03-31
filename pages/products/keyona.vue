<template>
  <div>
    <div class="large hidden-sm-and-down">
      <template>
        <v-parallax height="300" src="/machinery6.jpg"></v-parallax>
      </template>
      <v-container class="about">
        <v-row>
          <v-card
            elevation="6"
            shaped
            width="100%"
          >
            <v-container>
              <h1 class="grey--text text--darken-2">Keyona Superior - Special Maize Meal</h1>
              <v-divider class="mt-3 mb-3"></v-divider>
              <v-card class="ma-auto elevation-4" shaped color="#e4dc44" width="500" flat>
                <v-img src="/products/keyona-superior-maize.png" max-width="500"></v-img>
              </v-card>
              <v-data-table
                :custom-filter="filterOnlyCapsText"
                :headers="headers"
                :items="products"
                :search="search"
                class="elevation-0"
                item-key="name"
              >
                <template #top>
                  <v-text-field
                    v-model="search"
                    class="mx-4"
                    label="Search (UPPER CASE ONLY)"
                  ></v-text-field>
                </template>
              </v-data-table>
            </v-container>
            <v-btn class="ma-6">Download Brochure</v-btn>
            <v-dialog
              v-model="dialog"
              width="800"
            >
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                  color="red lighten-2"
                  dark
                  v-bind="attrs"
                  v-on="on"
                >
                  Nutritional Information
                </v-btn>
              </template>

              <v-card>
                <v-card-title class="text-h5 grey lighten-2">
                  Keyona Superior - Special Maze Meal
                </v-card-title>

                <v-card-text>
                  <h4 class="text-center">Typical Nutritional Information <br> Serving size: 100g meal (Uncooked)</h4>
                  <v-simple-table>
                    <template v-slot:default>
                      <thead>
                      <tr>
                        <th class="text-left">
                        </th>
                        <th class="text-left">
                          Per Serving
                        </th>
                        <th class="text-left">
                        </th>
                        <th class="text-left">
                          %RDA
                        </th>
                      </tr>
                      </thead>
                      <tbody>
                      <tr
                        v-for="item in items"
                        :key="item.name"
                      >
                        <td>{{ item.name }}</td>
                        <td>{{ item.serving }}</td>
                        <td>{{ item.weight }}</td>
                        <td>{{ item.rda }}</td>
                      </tr>
                      </tbody>
                    </template>
                  </v-simple-table>
                </v-card-text>

                <v-divider></v-divider>
                <p class="pa-3 text-center">RDA = Recommended Dietary Allowance for individuals 13 years and older.</p>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn
                    color="darkgreen"
                    text
                    @click="dialog = false"
                  >
                    Close
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
            <v-btn class="ml-6">Download Nutritional Information</v-btn>
          </v-card>
        </v-row>
      </v-container>
      <ProductCategory />
    </div>

    <!-- Mobile Design Viewport -->
    <div class="mobile hidden-md-and-up">
      <v-toolbar color="#e4dc44" height="160"></v-toolbar>
      <v-container class="about">
        <v-row>
          <v-card flat tile>
            <v-container>
              <h1 class="grey--text text--darken-2">Keyona Superior - Special Maize Meal</h1>
              <v-divider class="mt-3 mb-3"></v-divider>
              <v-card class="ma-auto elevation-4" shaped color="#e4dc44" width="500" flat>
                <v-img src="/products/keyona-superior-maize.png" max-width="500"></v-img>
              </v-card>
              <v-data-table
                :custom-filter="filterOnlyCapsText"
                :headers="headers"
                :items="products"
                :search="search"
                class="elevation-0"
                item-key="name"
              >
                <template #top>
                  <v-text-field
                    v-model="search"
                    class="mx-4"
                    label="Search (UPPER CASE ONLY)"
                  ></v-text-field>
                </template>
              </v-data-table>
            </v-container>
            <v-btn class="ml-3" small rounded>Download Brochure</v-btn>
            <v-dialog
              v-model="dialog"
              width="800"
            >
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                  class="ml-3 mt-2"
                  color="darkgreen"
                  dark
                  small
                  rounded
                  v-bind="attrs"
                  v-on="on"
                >
                  Nutritional Information
                </v-btn>
              </template>

              <v-card>
                <v-card-title class="text-h5 grey lighten-2">
                  Keyona Superior - Special Maze Meal
                </v-card-title>

                <v-card-text>
                  <h4 class="text-center">Typical Nutritional Information <br> Serving size: 100g meal (Uncooked)</h4>
                  <v-simple-table>
                    <template v-slot:default>
                      <thead>
                      <tr>
                        <th class="text-left">
                        </th>
                        <th class="text-left">
                          Per Serving
                        </th>
                        <th class="text-left">
                        </th>
                        <th class="text-left">
                          %RDA
                        </th>
                      </tr>
                      </thead>
                      <tbody>
                      <tr
                        v-for="item in items"
                        :key="item.name"
                      >
                        <td>{{ item.name }}</td>
                        <td>{{ item.serving }}</td>
                        <td>{{ item.weight }}</td>
                        <td>{{ item.rda }}</td>
                      </tr>
                      </tbody>
                    </template>
                  </v-simple-table>
                </v-card-text>

                <v-divider></v-divider>
                <p class="pa-3 text-center">RDA = Recommended Dietary Allowance for individuals 13 years and older.</p>
                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn
                    color="darkgreen"
                    text
                    @click="dialog = false"
                  >
                    Close
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
            <v-btn class="ml-3 mt-2" small rounded>Download Nutritional Information</v-btn>
          </v-card>
        </v-row>
      </v-container>
      <ProductCategory />
    </div>
  </div>
</template>

<script>
export default {
  name: "KeyonaMaize",
  data() {
    return {
      search: '',
      dialog: false,
      products: [
        {
          name: '80kg',
          product_range: 'SPK010',
          barcode: '6009608990717',
          baler: '',
          case: 12,
        },
        {
          name: '50kg',
          product_range: 'SPK009',
          barcode: '6009608990700',
          baler: '',
          case: 21,
        },
        {
          name: '25kg',
          product_range: 'SPK008',
          barcode: '6009608990694',
          baler: '',
          case: 45,
        },
        {
          name: '12.5kg',
          product_range: 'SPK007',
          barcode: '6009608990687',
          baler: '',
          case: 84,
        },
        {
          name: '10kg',
          product_range: 'SPK005',
          barcode: '6009608990670',
          baler: '',
          case: 104,
        },
        {
          name: '5kg Poly',
          product_range: 'SPK003',
          barcode: '6009608990649',
          baler: '',
          case: 195,
        },
      ],
      items: [
        {
          name: 'Energy',
          serving: '1445',
          weight: '(kj)',
          rda: '-',
        },
        {
          name: 'Protein',
          serving: '6.0',
          weight: '(g)',
          rda: '11%',
        },
        {
          name: 'Glycaemic Carbohydrate',
          serving: '72.2',
          weight: '(g)',
          rda: '-',
        },
        {
          name: '- Of which total sugars',
          serving: '2',
          weight: '',
          rda: '',
        },
        {
          name: 'Total Fat',
          serving: '2.7',
          weight: '(g)',
          rda: '-',
        },
        {
          name: '-  of which Saturated Fat',
          serving: '0.5',
          weight: '(g)',
          rda: '-',
        },
        {
          name: '-  of which Trans Fat',
          serving: '<0.01',
          weight: '(g)',
          rda: '-',
        },
        {
          name: '-  of which monounsaturated fat',
          serving: '0.9',
          weight: '(g)',
          rda: '-',
        },
        {
          name: '-  of which polyunsaturated fat',
          serving: '1.4',
          weight: '(g)',
          rda: '-',
        },
        {
          name: 'Cholesterol',
          serving: '<1>',
          weight: '(mg)',
          rda: '-',
        },
        {
          name: 'Dietary Fibre',
          serving: '4.6',
          weight: '(g)',
          rda: '',
        },
        {
          name: '-  of which insoluble fibre',
          serving: '0.9',
          weight: '(g)',
          rda: '',
        },
        {
          name: '-  of which soluble fibre',
          serving: '0.9',
          weight: '(g)',
          rda: '',
        },
        {
          name: 'Total Sodium',
          serving: '<6',
          weight: '(mg)',
          rda: '-',
        },
        {
          name: 'Vitamin A',
          serving: '188',
          weight: '(mcg)',
          rda: '21%',
        },
        {
          name: 'Vit B1 (Thiamine)',
          serving: '0.4',
          weight: '(mg)',
          rda: '33%',
        },
        {
          name: 'Vit B2 (Riboflavien)',
          serving: '0.2',
          weight: '(mg)',
          rda: '15%',
        },
        {
          name: 'Vit b3 (Niacin)',
          serving: '3.79',
          weight: '(mg)',
          rda: '20%',
        },
        {
          name: 'Vit B6 (Pyridoxine)',
          serving: '0.4',
          weight: '(mg)',
          rda: '24%',
        },
      ],
    }
  },
  computed: {
    headers() {
      return [
        {
          text: 'Packaging',
          align: 'start',
          sortable: false,
          value: 'name',
        },
        {
          text: 'Product Range',
          value: 'product_range',
          filter: value => {
            if (!this.calories) return true

            return value < parseInt(this.calories)
          },
        },
        {text: 'Barcode Single Unit', value: 'barcode'},
        {text: 'Barcode Baler', value: 'baler'},
        {text: 'Case Per Pallet', value: 'case'},
      ]
    },
  },
  methods: {
    filterOnlyCapsText(value, search, item) {
      return value != null &&
        search != null &&
        typeof value === 'string' &&
        value.toString().toLocaleUpperCase().includes(search)
    },
  },
}
</script>

<style scoped>
.container {
}

.about {
  margin-top: -150px;
}
</style>
