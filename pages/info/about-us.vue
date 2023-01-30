<template>
  <div>
    <template>
      <v-parallax height="300" src="/entrance.jpg"></v-parallax>
    </template>
    <v-container class="about">
        <v-card
          elevation="6"
          shaped
        >
          <v-container>
            <h1 class="grey--text text--darken-2">About Us</h1>
            <v-divider class="mt-2 mb-2"></v-divider>
            <p class="grey--text text--darken-2">Eendag Meule Bothaville (Pty) Ltd, is a medium sized maize mill in the
              town of Bothaville in the Free State –
              South Africa. Bothaville is widely recognised as the maize capital of South Africa and we purchase 100% of
              our raw
              materials from within the Bothaville district. </p>

            <p class="grey--text text--darken-2">The company was established in <b>August 2006</b> and actively
              commenced production in <b>May 2008</b>. We recently upgraded our mill and increased our capacity to <b>60 tons per hour</b>.
              Eendag Meule
              Bothaville (Pty) Ltd is driven by customer satisfaction and we strive to keep customer relations strong by
              supplying the best range of quality products at competitive prices.</p>

            <p class="grey--text text--darken-2">Eendag Meule Bothaville (Pty) Ltd Meule installed a Westweigh Systems
              fully automatic Premiertech Chronos bag
              placing system recently. With unrivalled speed and reliability, Westweigh Systems enables us to provide
              fast,
              quality service to our customers. </p>

            <p class="grey--text text--darken-2"><b>Early 2018 we installed a Naks Extrusion plant on site and planning
              more extrusion projects.</b></p>

            <p class="grey--text text--darken-2">We are also passionate about going green and have already completed
              Phase 1 of our green plan, which sees two of
              our 3 mills running on solar power. Phase 2 is in planning and will result in all our operations running
              off solar
              power in late 2019.</p>

            <p class="grey--text text--darken-2">We at Eendag Meule Bothaville (Pty) Ltd believe in finding the balance
              between technology and manual labour with
              a group of 118 full time employees reaping the rewards of a positive work ethic. We believe we have all
              the
              ingredients to build a mill which will benefit not only to our community, but also to our great nation and
              surrounding countries.</p>
            <v-card max-width="700" class="ma-auto pa-3">
              <v-img src="/new-machines.jpg" max-height="500" contain></v-img>
            </v-card>
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
  name: "AboutUs"
}
</script>

<style scoped>
.about {
  margin-top: -150px;
}
</style>
