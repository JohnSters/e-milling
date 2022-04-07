<template>
  <v-container>
    <v-row>
      <v-col
        v-for="(item, i) in items"
        :key="i"
        cols="12"
        sm="4"
      >
        <v-card class="pa-4">
          {{ item.title }}
          <v-img :src="item.img"></v-img>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>

export default {
  name: "ProductMain",
  data() {
    return {
      items: [
        // Super Life
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-1kg.jpg', description: '1 Kg' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-10kg.jpg', description: '10 Kg' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-12.5kg.jpg', description: '12,5 Kg' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-25kg.jpg', description: '25 Kg' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-50kg.jpg', description: '50 Kg' },
        { title: 'Super Life Maize Meal', img: '/products/super-life/super-life-80kg.jpg', description: '80 Kg' },
        // EM-Lucky
        { title: 'EM Lucky Super Maize Meal', img: '/products/em-lucky/em-lucky-1kg.jpg', description: '1 Kg' },
        { title: 'EM Lucky Super Maize Meal', img: '/products/em-lucky/em-lucky-2kg.jpg', description: '2 Kg' },
        { title: 'EM Lucky Super Maize Meal', img: '/products/em-lucky/em-lucky-10kg.jpg', description: '10 Kg' },
        { title: 'EM Lucky Super Maize Meal', img: '/products/em-lucky/em-lucky-12kg.jpg', description: '12,5 Kg' },
        { title: 'EM Lucky Super Maize Meal', img: '/products/em-lucky/em-lucky-25kg.jpg', description: '25 Kg' },
        { title: 'EM Lucky Super Maize Meal', img: '/products/em-lucky/em-lucky-50kg.jpg', description: '50 Kg' },
        { title: 'EM Lucky Super Maize Meal', img: '/products/em-lucky/em-lucky-80kg.jpg', description: '80 Kg' },
        // Keyona
        { title: 'Keyona Superior Maize Meal', img: '/products/keyona/keyona-10kg.jpg', description: '10 Kg' },
        { title: 'Keyona Superior Maize Meal', img: '/products/keyona/keyona-12kg.jpg', description: '12,5 Kg' },
        { title: 'Keyona Superior Maize Meal', img: '/products/keyona/keyona-25kg.jpg', description: '25 Kg' },
        { title: 'Keyona Superior Maize Meal', img: '/products/keyona/keyona-50kg.jpg', description: '50 Kg' },
        { title: 'Keyona Superior Maize Meal', img: '/products/keyona/keyona-80kg.jpg', description: '80 Kg' },
      ]
    }
  },
}
</script>

<style scoped>
.row {
  display: flex;
  flex-wrap: wrap;
  padding: 0 4px;
}

/* Create four equal columns that sits next to each other */
.column {
  flex: 25%;
  max-width: 25%;
  padding: 0 4px;
}

.column img {
  margin-top: 8px;
  vertical-align: middle;
  width: 100%;
}

/* Responsive layout - makes a two column-layout instead of four columns */
@media screen and (max-width: 800px) {
  .column {
    flex: 50%;
    max-width: 50%;
  }
}

/* Responsive layout - makes the two columns stack on top of each other instead of next to each other */
@media screen and (max-width: 600px) {
  .column {
    flex: 100%;
    max-width: 100%;
  }
}
</style>
