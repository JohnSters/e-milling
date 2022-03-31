<template>
  <div>
    <div class="large hidden-sm-and-down">
      <template>
        <v-parallax height="300" src="/machinery5.jpg"></v-parallax>
      </template>
      <v-container class="about">
        <v-row>
          <v-card
            elevation="6"
            shaped
            width="100%"
          >
            <v-container>
              <h1 class="grey--text text--darken-2">Life Super Maize Meal</h1>
              <v-divider class="mt-3 mb-3"></v-divider>
              <v-card class="ma-auto elevation-4" shaped color="red" width="500" flat>
                <v-img src="/products/life-super-maize-meal.png" max-width="500"></v-img>
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
                  Life Super Maize Meal
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
    <!-- Mobile design viewport -->
    <div class="mobile hidden-md-and-up">
      <v-toolbar class="hidden-md-and-up" color="red" height="160"></v-toolbar>
      <v-container class="about">
        <v-row>
          <v-card flat tile>
            <v-container>
              <h1 class="grey--text text--darken-2">Life Super Maize Meal</h1>
              <v-divider class="mt-3 mb-3"></v-divider>
              <v-card class="ma-auto elevation-4" shaped color="red" width="500" flat>
                <v-img src="/products/life-super-maize-meal.png" max-width="500"></v-img>
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
                  Life Super Maize Meal
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
            <v-btn class="ml-3 mt-2" rounded small>Download Nutritional Information</v-btn>
          </v-card>
        </v-row>
      </v-container>
      <ProductCategory />
    </div>
  </div>
</template>

<script>
export default {
  name: "LifeMaize",
  data() {
    return {
      search: '',
      dialog: false,
      products: [
        {
          name: '80kg',
          product_range: 'SULF010',
          barcode: '6009608992803',
          baler: '',
          case: 12,
        },
        {
          name: '50kg',
          product_range: 'SULF009',
          barcode: '6009608992797',
          baler: '',
          case: 21,
        },
        {
          name: '25kg',
          product_range: 'SULF008',
          barcode: '6009608992780',
          baler: '',
          case: 45,
        },
        {
          name: '12.5kg',
          product_range: 'SULF007',
          barcode: '6009608992773',
          baler: '',
          case: 84,
        },
        {
          name: '10kg',
          product_range: 'SULF005',
          barcode: '6009608992766',
          baler: '',
          case: 104,
        },
        {
          name: '5kg Poly',
          product_range: 'SULF003',
          barcode: '6009608992759',
          baler: '',
          case: 195,
        },
        {
          name: '4 x 5kg',
          product_range: 'SULR004',
          barcode: '6009608992759',
          baler: '16009608992756',
          case: 60,
        },
        {
          name: '4 x 2.5kg',
          product_range: 'SULR002',
          barcode: '6009608990984',
          baler: '16009608992749',
          case: 96,
        },
        {
          name: '10 x 1kg',
          product_range: 'SULR001',
          barcode: '6009608992735',
          baler: '16009608992732',
          case: 90,
        },
      ],
      items: [
        {
          name: 'Energy',
          serving: '1430',
          weight: '(kj)',
          rda: '12%',
        },
        {
          name: 'Protein',
          serving: '6.8',
          weight: '(g)',
          rda: '-',
        },
        {
          name: 'Carbohydrate',
          serving: '72.2',
          weight: '(g)',
          rda: '-',
        },
        {
          name: 'Total Fat',
          serving: '1.6',
          weight: '(g)',
          rda: '-',
        },
        {
          name: '-  Saturated Fat',
          serving: '0.2',
          weight: '(g)',
          rda: '-',
        },
        {
          name: '-  Trans Fatty Acids',
          serving: '0',
          weight: '(g)',
          rda: '-',
        },
        {
          name: '-  Trans Fatty Acids',
          serving: '0',
          weight: '(g)',
          rda: '-',
        },
        {
          name: 'Total Dietary Fibre',
          serving: '3.2',
          weight: '(g)',
          rda: '-',
        },
        {
          name: 'Sodium',
          serving: '2',
          weight: '(mg)',
          rda: '',
        },
        {
          name: 'Vitamin A',
          serving: '188',
          weight: '(mcg)',
          rda: '21%',
        },
        {
          name: 'Thiamine',
          serving: '0.31',
          weight: '(mg)',
          rda: '26%',
        },
        {
          name: 'Riboflavien',
          serving: '0.15',
          weight: '(mg)',
          rda: '14%',
        },
        {
          name: 'Niacin',
          serving: '2.97',
          weight: '(mg)',
          rda: '19%',
        },
        {
          name: 'Pyridoxine',
          serving: '0.39',
          weight: '(mg)',
          rda: '30%',
        },
        {
          name: 'Folic Acid',
          serving: '189',
          weight: '(mcg)',
          rda: '47%',
        },
        {
          name: 'Iron',
          serving: '3.79',
          weight: '(mg)',
          rda: '21%',
        },
        {
          name: 'Zinc',
          serving: '1.89',
          weight: '(mg)',
          rda: '17%',
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
