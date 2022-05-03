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
              <h1 class="grey--text text--darken-2">Hippo Samp</h1>
              <v-divider class="mt-3 mb-3"></v-divider>
                <v-card class="ma-auto elevation-4" shaped width="500" flat>
                  <v-img
                    transition="fade-transition"
                    src="/products/hippo-samp-combo.jpg"
                    lazy-src="/products/hippo-samp-combo.jpg"
                    aspect-ratio="1"
                    class="grey lighten-2"
                    max-width="500"
                    max-height="350"
                  >
                    <template v-slot:placeholder>
                      <v-row
                        class="fill-height ma-0"
                        align="center"
                        justify="center"
                      >
                        <v-progress-circular
                          indeterminate
                          color="grey lighten-5"
                        ></v-progress-circular>
                      </v-row>
                    </template>
                  </v-img>
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
            <v-btn href="/downloads/eendag-meule-broshure.pdf" download="" class="ma-6">Download Brochure</v-btn>
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
            <v-btn href="/downloads/nutritional-values.docx" download="" class="ml-6">Download Nutritional Information</v-btn>
          </v-card>
        </v-row>
      </v-container>
      <ProductCategory />
    </div>

    <!-- Mobile Design Viewport -->
    <div class="mobile hidden-md-and-up">
      <v-toolbar color="blue" height="160"></v-toolbar>
      <v-container class="about">
        <v-row>
          <v-card flat tile>
            <v-container>
              <h1 class="grey--text text--darken-2">Hippo Samp</h1>
              <v-btn to="product-main" class="blue--text" text>Back to Product Page</v-btn>
              <v-divider class="mt-3 mb-3"></v-divider>
              <v-card class="ma-auto elevation-4" shaped width="500" flat>
                <v-img
                  transition="fade-transition"
                  src="/products/hippo-samp-combo.jpg"
                  lazy-src="/products/hippo-samp-combo.jpg"
                  aspect-ratio="1"
                  class="grey lighten-2"
                  max-width="500"
                  max-height="350"
                >
                  <template v-slot:placeholder>
                    <v-row
                      class="fill-height ma-0"
                      align="center"
                      justify="center"
                    >
                      <v-progress-circular
                        indeterminate
                        color="grey lighten-5"
                      ></v-progress-circular>
                    </v-row>
                  </template>
                </v-img>
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
            <v-btn href="/downloads/Eendag Meule Brochure 2021.pdf" download class="ml-3" small rounded>Download Brochure</v-btn>
            <v-dialog
              v-model="dialog"
              width="800"
            >
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                  class="ml-3 mt-2"
                  color="darkgreen"
                  dark
                  rounded
                  small
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
                  <v-btn
                    color="darkgreen"
                    dark
                    @click="dialog = false"
                  >
                    Close
                  </v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
            <v-btn href="/downloads/nutritional-values.docx" download="" class="ml-3 mt-2" small rounded>Download Nutritional Information</v-btn>
          </v-card>
        </v-row>
      </v-container>
      <ProductCategory />
    </div>

  </div>
</template>

<script>
export default {
  name: "HippoSamp",
  data() {
    return {
      search: '',
      dialog: false,
      products: [
        {
          name: '25kg',
          product_range: 'STA008',
          barcode: '6009608990847',
          baler: '',
          case: 45,
        },
        {
          name: '12.5kg',
          product_range: 'STA006',
          barcode: '6009608990816',
          baler: '',
          case: 84,
        },
        {
          name: '10kg',
          product_range: 'STA004',
          barcode: '6009608990809',
          baler: '',
          case: 104,
        },
        {
          name: '5kg',
          product_range: 'STA003',
          barcode: '6009608990793',
          baler: '',
          case: 195,
        },
        {
          name: '8 x 2.5kg',
          product_range: 'STA002',
          barcode: '6009608990786',
          baler: '26009608990780',
          case: 50,
        },
        {
          name: '20 x 1kg',
          product_range: 'STA001',
          barcode: '6009608990779',
          baler: '26009608990773',
          case: 50,
        },
      ],
      items: [
        {
          name: 'Energy',
          serving: '924',
          weight: '(kj)',
          rda: '',
        },
        {
          name: 'Protein',
          serving: '4.8',
          weight: '(g)',
          rda: '9%',
        },
        {
          name: 'Carbohydrates',
          serving: '47.3',
          weight: '(g)',
          rda: '-',
        },
        {
          name: ' Total Fat',
          serving: '0.4',
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
          name: 'Cholesterol',
          serving: '0',
          weight: '(mg)',
          rda: '-',
        },
        {
          name: 'Total Dietary Fibre',
          serving: '1.8',
          weight: '(g)',
          rda: '-',
        },
        {
          name: 'Sodium',
          serving: '680',
          weight: '(mg)',
          rda: '-',
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
          sortable: true,
          value: 'name',
        },
        {
          text: 'Product Range',
          value: 'product_range',
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
