<template>
  <v-div>
    <h1>Lucky Super Maize Meal</h1>
    <v-data-table
      :headers="headers"
      :items="desserts"
      item-key="name"
      class="elevation-1"
      :search="search"
      :custom-filter="filterOnlyCapsText"
    >
      <template v-slot:top>
        <v-text-field
          v-model="search"
          label="Search (UPPER CASE ONLY)"
          class="mx-4"
        ></v-text-field>
      </template>
      <template>
        <tr>
          <td>
            <v-text-field
              v-model="calories"
              type="number"
              label="Less than"
            ></v-text-field>
          </td>
          <td colspan="4">
          </td>
        </tr>
      </template>
    </v-data-table>
  </v-div>
</template>

<script>
export default {
  name: "LuckyMaize",
  data () {
    return {
      search: '',
      calories: '',
      desserts: [
        {
          name: '80kg',
          product_range: 'SUL010',
          barcode: '6009608990960',
          baler: '',
          case: 12,
        },
        {
          name: '50kg',
          product_range: 'SUL009',
          barcode: '6009608990953',
          baler: '',
          case: 21,
        },
        {
          name: '25kg',
          product_range: 'SUL008',
          barcode: '6009608990946',
          baler: '',
          case: 45,
        },
        {
          name: '12.5kg',
          product_range: 'SUL007',
          barcode: '6009608990939',
          baler: '',
          case: 84,
        },
        {
          name: '10kg',
          product_range: 'SUL005',
          barcode: '6009608990922',
          baler: '',
          case: 104,
        },
        {
          name: '5kg Poly',
          product_range: 'SUL003',
          barcode: '6009608990991',
          baler: '',
          case: 195,
        },
        {
          name: '4 x 5kg',
          product_range: 'SUL003',
          barcode: '6009608990991',
          baler: '16009608990998',
          case: 60,
        },
        {
          name: '4 x 2.5kg',
          product_range: 'SUL002',
          barcode: '6009608990984',
          baler: '16009608990981',
          case: 96,
        },
        {
          name: '10 x 1kg',
          product_range: 'SUL001',
          barcode: '6009608990977',
          baler: '16009608990974',
          case: 90,
        },
      ],
    }
  },
  computed: {
    headers () {
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
        { text: 'Barcode Single Unit', value: 'barcode' },
        { text: 'Barcode Baler', value: 'baler' },
        { text: 'Case Per Pallet', value: 'case' },
      ]
    },
  },
  methods: {
    filterOnlyCapsText (value, search, item) {
      return value != null &&
        search != null &&
        typeof value === 'string' &&
        value.toString().toLocaleUpperCase().includes(search)
    },
  },
}
</script>

<style scoped>

</style>
