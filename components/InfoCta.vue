<template>
  <div class="info-cta">
    <v-container>
      <h3>Uber for Business</h3>
      <p class="mt-5 mb-7">
        Transform the way your company moves and feeds its people.
      </p>
      <v-btn large tile class="capitalize-btn" dark color="#000">See how</v-btn>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style>
.info-cta {
  margin-top: -30px;
  background-image: linear-gradient(
      45deg,
      rgba(255, 255, 255, 0.2),
      transparent
    ),
    url(~/assets/images/see-how.png);
  background-size: cover, cover;
  background-repeat: no-repeat, no-repeat;
  background-position: center, center;
  padding: 70px 0;
}
.info-cta h3 {
  font-size: 36px;
  line-height: 1.4;
  font-weight: 500;
}
</style>
