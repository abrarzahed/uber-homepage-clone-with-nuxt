<template>
  <div class="main-menu">
    <div class="menu-items-left">
      <h3 class="logo mr-8">Uber</h3>
      <v-menu transition="slide-y-transition" bottom tile min-width="200">
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            small
            class="capitalize-btn"
            rounded
            dark
            v-bind="attrs"
            v-on="on"
            depressed
          >
            Company <v-icon right>mdi-chevron-down</v-icon>
          </v-btn>
        </template>
        <v-list dense>
          <v-list-item
            class="dropdown-item"
            dense
            link
            v-for="(item, index) in companyItems"
            :key="index"
          >
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
      <v-btn
        small
        class="capitalize-btn"
        v-for="(item, i) in menuItems"
        :key="i"
        rounded
        dark
        depressed
        >{{ item.title }}</v-btn
      >
    </div>
    <div class="menu-items-right">
      <v-btn small depressed dark rounded class="capitalize-btn"
        ><v-icon left>mdi-web</v-icon>EN</v-btn
      >
      <v-menu
        transition="slide-y-transition"
        bottom
        tile
        right
        max-height="320"
        min-width="250"
      >
        <template v-slot:activator="{ on, attrs }">
          <v-btn
            small
            class="capitalize-btn"
            rounded
            dark
            v-bind="attrs"
            v-on="on"
            depressed
          >
            <v-icon left>mdi-dots-grid</v-icon> Products
          </v-btn>
        </template>
        <v-list dense>
          <!-- ---------------------------------------- -->

          <v-list-item
            class="bordered-dropdown-item"
            link
            v-for="(item, i) in productsItems"
            :key="i"
          >
            <v-list-item-icon class="mr-5">
              <v-icon class="text-h6" color="#000">{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title class="product-dropdown-item">{{
                item.title
              }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <!-- ---------------------------------------- -->
        </v-list>
      </v-menu>
      <v-btn depressed small dark rounded class="capitalize-btn ml-2"
        ><v-icon left>mdi-account</v-icon>Log in</v-btn
      >
      <v-btn
        depressed
        dark
        color="#fff"
        rounded
        class="capitalize-btn black--text"
        >Sign up</v-btn
      >
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    menuItems: [
      { title: "Safety", url: "#" },
      { title: "Help", url: "#" },
      { title: "Covid-19-resources", url: "#" },
    ],
    companyItems: [
      { title: "About us" },
      { title: "Our offering" },
      { title: "How Uber works" },
      { title: "Global citizenship" },
      { title: "Newsroom" },
      { title: "Investor relations" },
      { title: "Blog" },
      { title: "Careers" },
    ],
    productsItems: [
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
  }),
};
</script>
<style>
.test {
  box-shadow: 0 !important;
}
.logo {
  font-size: 24px;
  font-weight: 400;
}
.main-menu {
  display: flex;
  align-self: center;
  justify-content: space-between;
}
.menu-items-left {
  display: flex;
  align-items: center;
  gap: 4px;
}

.dropdown-item * {
  font-size: 14px;
  font-weight: 400;
  color: #444;
}
.dropdown-item:hover * {
  color: #000;
}
.menu-items-right {
  display: flex;
  align-items: center;
  gap: 4px;
}
.bordered-dropdown-item {
  border-bottom: 1px solid #ddd;
}
.product-dropdown-item {
  font-size: 20px !important;
  font-weight: 500 !important;
}
.v-menu__content.theme--light.v-menu__content--fixed.menuable__content__active {
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2) !important;
  top: 64px !important;
}
</style>
