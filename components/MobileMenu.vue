<template>
  <div class="mobile-menu">
    <h3 class="logo">Uber</h3>

    <div class="mobile-menu-items">
      <v-btn
        @click="openDialog"
        depressed
        small
        dark
        rounded
        class="capitalize-btn ml-2"
        ><v-icon left>mdi-account</v-icon>Log in</v-btn
      >
      <v-btn
        @click="openDialog"
        depressed
        small
        dark
        color="#fff"
        rounded
        class="capitalize-btn black--text"
        >Sign up</v-btn
      >
      <v-btn @click="openSideMenu" x-small dark depressed text>
        <v-icon>mdi-menu</v-icon>
      </v-btn>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  methods: {
    openDialog() {
      this.$emit("openDialog");
    },
    openSideMenu() {
      this.$emit("openSideMenu");
    },
  },
};
</script>

<style>
.mobile-menu {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.mobile-menu-items {
  display: flex;
  gap: 10px;
  align-items: center;
}
</style>
