<template>
  <v-container>
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
  </v-container>
</template>

<script>
export default {
  name: "product-range",
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
          iron: ''
        },
        {
          name: '50kg',
          product_range: 'SUL009',
          barcode: '6009608990953',
          baler: '',
          case: 21,
          iron: ''
        },
        {
          name: '25kg',
          product_range: 'SUL008',
          barcode: '6009608990946',
          baler: '',
          case: 45,
          iron: ''
        },
        {
          name: '12.5kg',
          product_range: 'SUL007',
          barcode: '6009608990939',
          baler: '',
          case: 84,
          iron: ''
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
        { text: 'View Product', value: 'iron' },
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
