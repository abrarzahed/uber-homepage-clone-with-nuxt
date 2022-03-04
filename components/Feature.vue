<template>
  <div class="feature">
    <v-container>
      <h2 class="mb-10 section-title">Focused on safety, wherever you go</h2>
      <div class="feature-container">
        <div class="feature-section-left">
          <img src="~/assets/images/feature-section-left-img.png" alt="" />
          <h4 class="my-4">Our commitment to your safety</h4>
          <p>
            With every safety feature and every standard in our Community
            Guidelines, we're committed to helping to create a safe environment
            for our users.
          </p>
          <div class="feature-section-link-group mt-10">
            <AnimatedLink :link="link1" />
            <AnimatedLink :link="link2" />
          </div>
        </div>
        <div class="feature-section-right">
          <img src="~/assets/images/feature-section-right.png" alt="" />
          <h4 class="my-4">Our commitment to your safety</h4>
          <p>
            The app is available in thousands of cities worldwide, so you can
            request a ride even when you’re far from home.
          </p>
          <div class="feature-section-link-group mt-10">
            <AnimatedLink :link="link3" />
          </div>
        </div>
      </div>
      <FeaturedCard />
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      link1: {
        url: "#",
        text: "Read about our Community Guidelines",
      },
      link2: {
        url: "#",
        text: "See all safety features",
      },
      link3: {
        url: "#",
        text: "View all cities",
      },
    };
  },
};
</script>

<style>
.feature {
  padding: 70px 0;
}

.feature-container {
  display: flex;
  gap: 34px;
  align-items: stretch;
}
.feature-section-left {
  flex-basis: 50%;
}
.feature-section-right {
  flex-basis: 50%;
}
.feature-container img {
  width: 100%;
  object-fit: cover;
}
.feature-container h4 {
  font-size: 20px;
  font-weight: 500;
}
.feature-section-link-group {
  display: flex;
  gap: 30px;
}
</style>
