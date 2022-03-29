<template>
  <div>
    <template>
      <v-parallax height="300" src="/office-inside.jpg"></v-parallax>
    </template>
    <v-container class="power">
      <v-card elevation="6" shaped>
        <v-container>
          <h1>Green Power</h1>
          <v-divider class="mt-2 mb-2"></v-divider>
          <p>Solar energy is a natural form of energy which does not contribute to global warming. Unlike fossil fuels, solar panels don't release any greenhouse gases, carcinogens, carbon dioxide or other poisonous gases. Eendag Meule Bothaville (Pty) Ltd is one of few mills in Africa making use of solar power.</p>
          <p>The Eendag Meule Bothaville (Pty) Ltd solar project currently consists of 2526, 255 Watt solar panels and 11 x 60 Kwp string inverters, which generates between 2.5 and 3.5 Megawatt power per day.  This adds up to approximately 1 000 000 Kwh per year and an estimate of 31 973 Mwh for the 25-year life span of the solar plant. </p>
          <p>This green solution saves 1 226 400 kg of CO2 pollution per annum and 30 660 000 kg of CO2 emissions over a 25-year span. The estimated number of trees which need to be planted to offset those emissions, equals 4 882 trees per year.</p>
          <p>Recently Green energy is becoming progressively more popular due to the myriads of benefits it provides. It is a sustainable, reliable and comprehensive source of energy that requires little or no maintenance and provides long-term benefits.</p>
          <p>We are proudly going green and are planning further development which will result in all our mills running off solar power. </p>
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
  name: "GreenPower",
}
</script>

<style>
.power {
  margin-top: -150px;
}
</style>


