<template>
  <div class="tab">
    <h3 class="text-h3 font-weight-medium">
      Get in the driver’s <br />seat and get paid
    </h3>
    <p class="my-8">
      Drive on the platform with the largest network of active riders.
    </p>
    <v-btn large tile dark color="#000" class="capitalize-btn"
      >Sign up to drive</v-btn
    >
    <AnimatedLink class="mt-8" :link="link" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      link: { url: "#", text: "Learn more about driving and delivering" },
    };
  },
};
</script>

<style></style>
