<template>
  <div class="tab">
    <h3 class="text-h3 font-weight-medium">Discover delicious eats</h3>
    <p class="my-8 tab-desc">Order delivery from restaurants you love.</p>
    <div class="button-link-group">
      <v-btn large tile dark color="#000" class="capitalize-btn"
        >Order now</v-btn
      >
      <AnimatedLink :link="link" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      link: { url: "#", text: "Own a restaurant? Partner with Uber Eats" },
    };
  },
};
</script>

<style></style>
