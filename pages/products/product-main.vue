<template>
  <v-container>
    <h1 class="grey--text text--darken-2 text-center">View our wide range of top quality products.</h1>
    <v-divider class="ma-3 mb-6"></v-divider>

    <v-row>
      <!--  Large Screen View  -->
      <v-col
        cols="12"
        sm="6"
        class="hidden-md-and-down"
      >
        <h3 class="grey--text darken-2 text-center mb-2">Lucky Super Maize Meal</h3>
        <v-card class="green pa-2 rounded-tl-circle rounded-tr-circle elevation-4" height="423" link to="lucky">
          <v-img src="em-lucky-combo.jpg" lazy-src="em-lucky-combo.jpg" height="406"></v-img>
        </v-card>
      </v-col>
      <!-- Small Screen View -->
      <v-col
        cols="12"
        sm="6"
        class="hidden-sm-and-up"
      >
        <h3 class="grey--text darken-2 text-center mb-2">Lucky Super Maize Meal</h3>
        <v-card class="green pa-2 elevation-4" link to="lucky">
          <v-img src="em-lucky-combo.jpg" lazy-src="em-lucky-combo.jpg"></v-img>
        </v-card>
      </v-col>

      <!--  Large Screen View  -->
      <v-col
        cols="12"
        sm="6"
        class="hidden-md-and-down"
      >
        <h3 class="grey--text darken-2 text-center mb-2">Super Life Maize Meal</h3>
        <v-card class="red pa-2 rounded-tr-circle rounded-tl-circle elevation-4" height="423" link to="life">
          <v-img src="life-maize-combo.jpg" lazy-src="life-maize-combo.jpg" height="406"></v-img>
        </v-card>
      </v-col>

      <!-- Small Screen View -->
      <v-col
        cols="12"
        sm="6"
        class="hidden-sm-and-up"
      >
        <h3 class="grey--text darken-2 text-center mb-2">Super Life Maize Meal</h3>
        <v-card class="red pa-2 elevation-4" link to="life">
          <v-img src="life-maize-combo.jpg" lazy-src="life-maize-combo.jpg"></v-img>
        </v-card>
      </v-col>
      <!-- Large Screen View -->
      <v-col
        cols="12"
        sm="6"
        class="hidden-md-and-down"
      >
        <v-card class="yellow pa-2 rounded-0" height="405" flat link to="keyona">
          <v-img src="keyona-maize-combo.jpg" lazy-src="keyona-maize-combo.jpg" height="388"></v-img>
        </v-card>
        <h3 class="grey--text darken-2 text-center mt-2">Keyona Superior Maize Meal</h3>
      </v-col>
      <!-- Small Screen View -->
      <v-col
        cols="12"
        sm="6"
        class="hidden-sm-and-up"
      >
        <h3 class="grey--text darken-2 text-center mt-2">Keyona Superior Maize Meal</h3>
        <v-card class="yellow pa-2 rounded-0" flat link to="keyona">
          <v-img src="keyona-maize-combo.jpg" lazy-src="keyona-maize-combo.jpg" contain></v-img>
        </v-card>
      </v-col>

      <!-- Large Screen View -->
      <v-col
        cols="12"
        sm="6"
        class="hidden-md-and-down"
      >
        <v-card class="blue pa-2 rounded-0" height="405" flat link to="hippo">
          <v-img src="hippo-samp-combo.jpg" lazy-src="hippo-samp-combo.jpg" height="388" ></v-img>
        </v-card>
        <h3 class="grey--text darken-2 text-center mt-2">Hippo Samp</h3>
      </v-col>
      <!-- Small Screen View -->
      <v-col
        cols="12"
        sm="6"
        class="hidden-sm-and-up"
      >
        <h3 class="grey--text darken-2 text-center mt-2">Hippo Samp</h3>
        <v-card class="blue pa-2 rounded-0" flat link to="hippo">
          <v-img src="hippo-samp-combo.jpg" lazy-src="hippo-samp-combo.jpg" ></v-img>
        </v-card>
      </v-col>

    </v-row>

    <v-divider class="ma-3"></v-divider>
    <h1 class="text-center grey--text text--darken-2 font-weight-light">Looking for something special?</h1>
    <h4 class="text-center green--text text--darken-2 mb-3">Tel: <b class="orange--text">056-515-1309</b> to find out more!</h4>
    <v-row>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Plaasjapie Growwe Braaipap</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/niche1.png" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Plaasjapie Bittergrowwe Braaipap</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/niche2.png" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>

      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Plaasjapie Semelverrykte Braaipap</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/niche3.png" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Plaasjapie Growwe Geelmeel</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/niche4.png" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>
    </v-row>
    <v-row>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Eendag Yellow Maize</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/yellow.jpg" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>
      <v-hover v-slot="{ hover }">
        <v-col
          cols="12"
          md="3"
        >
          <p class="text-center">Chick a-Licious</p>
          <v-card class="pa-4" :elevation="hover ? 4 : 2" link>
            <v-img src="/products/chick.jpg" height="360"></v-img>
          </v-card>
        </v-col>
      </v-hover>
    </v-row>
    <ProductCategory />
  </v-container>
</template>

<script>

export default {
  name: "ProductMain",
  data() {
    return {
      items: [
        // Super Life
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-1kg.jpg', description: '1 Kg', link: '/products/life' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-10kg.jpg', description: '10 Kg', link: '/products/life' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-12kg.jpg', description: '12,5 Kg', link: '/products/life' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-25kg.jpg', description: '25 Kg', link: '/products/life' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-50kg.jpg', description: '50 Kg', link: '/products/life' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-80kg.jpg', description: '80 Kg', link: '/products/life' },
        // EM-Lucky
        { title: 'EM Lucky Maize Meal', img: '/products/em-lucky/em-lucky-1kg.jpg', description: '1 Kg', link: '/products/lucky' },
        { title: 'EM Lucky Maize Meal', img: '/products/em-lucky/em-lucky-2kg.jpg', description: '2 Kg',link: '/products/lucky' },
        { title: 'EM Lucky Maize Meal', img: '/products/em-lucky/em-lucky-10kg.jpg', description: '10 Kg', link: '/products/lucky' },
        { title: 'EM Lucky Maize Meal', img: '/products/em-lucky/em-lucky-12kg.jpg', description: '12,5 Kg', link: '/products/lucky' },
        { title: 'EM Lucky Maize Meal', img: '/products/em-lucky/em-lucky-25kg.jpg', description: '25 Kg', link: '/products/lucky' },
        { title: 'EM Lucky Maize Meal', img: '/products/em-lucky/em-lucky-50kg.jpg', description: '50 Kg', link: '/products/lucky' },
        { title: 'EM Lucky Maize Meal', img: '/products/em-lucky/em-lucky-80kg.jpg', description: '80 Kg', link: '/products/lucky' },
        // Keyona
        { title: 'Keyona Maize Meal', img: '/products/keyona/keyona-10kg.jpg', description: '10 Kg', link: '/products/keyona' },
        { title: 'Keyona Maize Meal', img: '/products/keyona/keyona-12kg.jpg', description: '12,5 Kg', link: '/products/keyona' },
        { title: 'Keyona Maize Meal', img: '/products/keyona/keyona-25kg.jpg', description: '25 Kg', link: '/products/keyona' },
        { title: 'Keyona Maize Meal', img: '/products/keyona/keyona-50kg.jpg', description: '50 Kg', link: '/products/keyona' },
        { title: 'Keyona Maize Meal', img: '/products/keyona/keyona-80kg.jpg', description: '80 Kg', link: '/products/keyona' },
        // Hippo
        { title: 'Hippo Samp', img: '/products/hippo/hippo-1kg.jpg', description: '1 Kg', link: '/products/hippo' },
        { title: 'Hippo Stamp', img: '/products/hippo/hippo-2kg.jpg', description: '2,5 Kg',link: '/products/hippo' },
        { title: 'Hippo Stamp', img: '/products/hippo/hippo-5kg.jpg', description: '5 Kg', link: '/products/hippo' },
        { title: 'Hippo Stamp', img: '/products/hippo/hippo-12kg.jpg', description: '12,5 Kg', link: '/products/hippo' },
        { title: 'Hippo Stamp', img: '/products/hippo/hippo-25kg.jpg', description: '25 Kg', link: '/products/hippo' },
      ]
    }
  },
}
</script>

<style scoped>

</style>
