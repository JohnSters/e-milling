<template>
  <div>
    <template>
      <v-parallax height="300" src="/office-inside.jpg"></v-parallax>
    </template>
    <v-container class="packing">
      <v-card elevation="6" shaped>
        <v-container>
          <h1>Packing Excellence</h1>
          <v-divider class="mt-2 mb-2"></v-divider>
          <p>Eendag Meule Bothaville (Pty) Ltd recently installed a Westweigh Systems fully automatic Premiertech Chronos bag placing system. This makes us the first mill in South Africa to install such a bagging system. The system consists of integrated dual head screw fed bagging scales, a Fuji robotic palletizer and semi-automatic pallet handling and wrapper system.</p>
          <p>With unrivalled speed and reliability, Westweigh Systems provides a peace of mind packing solution to continuously pack our maize meal.  Eendag Meule Bothaville (Pty) Ltd strives to provide fast, quality service to our customers. With packing speeds of 20 bags/min for 10kg and 12.5kg, up to 18 bags per minute for 25kg and 10 bags/min on 50kg; we are able to achieve that.</p>
          <p>At Eendag Meule Bothaville (Pty) Ltd, we believe in finding the balance between technology and manual labour. With world class technology and a group of 100 full time employees, we reap the reward of a positive work ethic.</p>
          <p>We believe that Eendag Meule Bothaville (Pty) Ltd has a success recipe which benefits our community, our customers, our nation and surrounding countries.</p>
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
  name: "PackingExcellence"
}
</script>

<style scoped>
.packing {
  margin-top: -150px;
}
</style>
