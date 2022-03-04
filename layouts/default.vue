<template>
  <v-app>
    <v-app-bar fixed dark app elevation="0">
      <v-container>
        <MenuBar />
      </v-container>
    </v-app-bar>
    <v-main>
      <!-- <v-container> -->
      <Nuxt />
      <!-- </v-container> -->
    </v-main>

    <v-footer dark color="#000">
      <v-container>
        <AppFooter />
        <span class="mt-5 caption"
          >&copy; {{ new Date().getFullYear() }} ||
          abrarzahed6986@gmail.com</span
        >
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {};
  },
};
</script>
