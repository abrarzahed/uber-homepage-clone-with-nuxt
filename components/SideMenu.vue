<template>
  <div class="side-menu pa-5">
    <span @click="closeSideMenu" class="font-weight-black">&times;</span>
    <v-list class="mt-10">
      <v-list-group :value="false">
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title class="font-weight-medium"
              >Company</v-list-item-title
            >
          </v-list-item-content>
        </template>

        <v-list-item dense v-for="(title, i) in links" :key="i" link>
          <v-list-item-title v-text="title"></v-list-item-title>
        </v-list-item>
      </v-list-group>
      <v-divider></v-divider>
      <v-list-item dense link>
        <v-list-item-title class="font-weight-bold">Safety</v-list-item-title>
      </v-list-item>
      <v-divider></v-divider>
      <v-list-item dense link>
        <v-list-item-title class="font-weight-bold">Help</v-list-item-title>
      </v-list-item>
      <v-divider></v-divider>
      <v-list-item dense link>
        <v-list-item-title class="font-weight-bold"
          >Covid-19-resources</v-list-item-title
        >
      </v-list-item>
      <v-divider></v-divider>

      <v-list-group :value="false" prepend-icon="mdi-dots-grid">
        <template v-slot:activator>
          <v-list-item-content>
            <v-list-item-title class="font-weight-medium"
              >productsLinks</v-list-item-title
            >
          </v-list-item-content>
        </template>

        <v-list-item dense v-for="(item, i) in productsLinks" :key="i" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-title v-text="item.title"></v-list-item-title>
        </v-list-item>
      </v-list-group>
    </v-list>
  </div>
</template>

<script>
export default {
  data() {
    return {
      links: [
        "About us",
        "Our offering",
        "How Uber works",
        "Global citizenship",
        "Newsroom",
        "Investor relations",
        "Blog",
        "Careers",
      ],
      productsLinks: [
        { title: "Home", icon: "mdi-home-variant-outline" },
        { title: "Ride", icon: "mdi-car-back" },
        { title: "Drive", icon: "mdi-car-speed-limiter" },
        { title: "Eat", icon: "mdi-food-fork-drink" },
        { title: "Bike & Scoot", icon: "mdi-bike-fast" },
        { title: "Transit", icon: "mdi-train" },
        { title: "Travel", icon: "mdi-bag-suitcase" },
        { title: "Business", icon: "mdi-bag-checked" },
        { title: "Money", icon: "mdi-cash" },
      ],
    };
  },
  methods: {
    closeSideMenu() {
      this.$emit("closeSideMenu");
    },
  },
};
</script>

<style>
.side-menu {
  width: 80%;
  height: 100%;
  position: fixed;
  top: 0;
  right: 0;
  background: #fff;
  z-index: 9;
  border-left: 2px solid #ccc;
  transition: transform 0.2s ease-in;
  transform: translateX(100%);
}
.side-menu.active {
  transform: translateX(0);
}
.side-menu span {
  position: absolute;
  top: 0;
  right: 30px;
  font-size: 40px;
}
</style>
