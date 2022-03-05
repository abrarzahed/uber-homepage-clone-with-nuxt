<template>
  <v-app>
    <v-app-bar fixed dark app elevation="0">
      <v-container>
        <MenuBar
          @openDialog="langDialog = true"
          @openLoginDialog="loginDialog = true"
        />
      </v-container>
    </v-app-bar>
    <v-main>
      <Nuxt />
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
    <LangDialog @closeDialog="closeDialog" :dialog="langDialog" />
    <LoginSignupDialog
      @closeSignInDialog="loginDialog = false"
      :dialog="loginDialog"
    />
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      langDialog: false,
      loginDialog: false,
    };
  },
  methods: {
    closeDialog() {
      this.langDialog = false;
    },
  },
};
</script>
