<template>
  <v-container>
    <h1 class="grey--text text--darken-2">View our wide range of top quality products.</h1>
    <v-divider class="ma-3 mb-6"></v-divider>

    <v-row>
      <v-col
        v-for="(item, i) in items"
        :key="i"
        cols="12"
        sm="3"
      >
        <v-hover v-slot="{ hover }" >
          <v-card
            :elevation="hover ? 2 : 4"
            :class="{ 'on-hover': hover }"
            shaped
            class="pa-4"
            width="300"
            height="460"
            link
            :to="item.link">
            <h3 class="text-center grey--text text--darken-2 mb-2">{{ item.title }}</h3>
            <v-img :src="item.img" :lazy-src="item.img" width="300" contain></v-img>
            <v-divider class="ma-3"></v-divider>
            <h4 class="text-center grey--text text--darken-2">{{ item.description }}</h4>
          </v-card>
        </v-hover>

      </v-col>
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
