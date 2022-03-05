<template>
  <div class="featured-cards">
    <div v-for="(card, i) in cards" :key="i" class="featured-card">
      <v-icon color="#000" x-large>{{ card.icon }}</v-icon>
      <h5 class="my-2">{{ card.heading }}</h5>
      <p>
        {{ card.desc }}
      </p>
      <AnimatedLink :link="card.link" class="mt-10" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          icon: "mdi-account-multiple-outline",
          heading: "About us",
          desc: `Find out how we started, what drives us, and how we’re remaining how the world moves.`,
          link: {
            url: "#",
            text: "Learn more about Uber",
          },
        },
        {
          icon: "mdi-newspaper-variant-outline",
          heading: "Newsroom",
          desc: `See announcements about our latest releases, initiatives, and partnerships.`,
          link: {
            url: "#",
            text: "Go to Newsroom",
          },
        },
        {
          icon: "mdi-home",
          heading: "Global citizenship",
          desc: `Read about our commitment to making a positive impact in the cities we serve.`,
          link: {
            url: "#",
            text: "See our partnerships",
          },
        },
      ],
    };
  },
};
</script>

<style>
.featured-cards {
  margin-top: 100px;
  display: flex;
  gap: 30px;
}
.featured-card h5 {
  font-size: 19px;
  font-weight: 500;
}
@media (max-width: 768px) {
  .featured-cards {
    margin-top: 100px;
    flex-direction: column;
    text-align: center;
  }
}
</style>
