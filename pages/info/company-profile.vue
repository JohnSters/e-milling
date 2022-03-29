<template>
  <div>
    <template>
      <v-parallax height="300" src="/office-inside.jpg"></v-parallax>
    </template>
    <v-container class="profile">
      <v-card elevation="6" shaped>
        <v-container>
          <h1>Company Profile</h1>
          <v-divider class="mt-2 mb-2"></v-divider>
          <p>Eendag Meule Bothaville (Pty) Ltd was established in August 2006 and actively commenced production in May 2008, with one 6 ton/hour mill.</p>
          <p>In 2011, Eendag Meule Bothaville (Pty) Ltd constructed a second 6 ton/per hour mill, soon bordering on running at full capacity.</p>
          <p>Our latest upgrade in 2015, led to the installation of a 15 ton/hour mill, and capacity was increased up to 30 tons per hour.</p>
          <p>Eendag Meule Bothaville (Pty) Ltd also installed a Westweigh Systems fully automatic Premiertech Chronos bag placing system. The system consists of integrated dual head screw fed bagging scales, a Fuji robotic palletizer and semi-automatic pallet handling and wrapper system.</p>
          <p>With unrivalled speed and reliability, Westweigh Systems provides a peace of mind packing solution to continuously pack our maize meal.  At speeds of 20 bags/min for 10kg and 12.5kg, up to 18 bags/min for 25kg and 10 bags/min on 50kg, Eendag Meule Bothaville (Pty) Ltd strives to provide fast, quality service to our customers.</p>
          <p>We currently provide job opportunities for approximately 118 full time employees, reaping the rewards of a positive work ethic. Our unbelievable growth over the past 10 years in this competitive global economic environment, can be attributed to our employees’ and management’s hard work and ‘never say die’ attitude. </p>

          <h3>Our Vision</h3>
          <h4>Passionate about being a leading milling company, and focusing on:</h4>

          <ul>
            <li>Quality</li>
            <li>Understanding our customers' needs</li>
            <li>Promoting care, concern and respect for our people</li>
          </ul>
          <br>
          <p>"A happy and passionate workforce providing a service to customers who believe in our products"</p>

          <h3>Our Values</h3>
          <h4>We value our people, strive for excellence and believe in being transparent and honest with our customers.</h4>

          <ul>
            <li><b>Integrity</b> - We build trust by acting with honesty and openness.</li>
            <li><b>Passion</b> - We are enthusiastic, positive and energetic in the pursuit of excellence.</li>
            <li><b>Happy Clients</b> - Best sales service, right quality, right price, on time!</li>
            <li><b>Happy Workforce</b> - Clear job descriptions, passionate in what we do, growing and learning, responsible and disciplined, safety first and reminiscent of a family.</li>
            <li><b>Safety First</b> - Safety above production - thinking of my fellow workers first by being resilient and sharp.</li>
            <li><b>Making Money</b> - Zero waste, no rework</li>
          </ul>
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
  name: "CompanyProfile"
}
</script>

<style scoped>
.profile {
  margin-top: -150px;
}
</style>
