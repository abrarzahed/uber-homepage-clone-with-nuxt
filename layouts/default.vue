<template>
  <v-app>
    <v-app-bar fixed dark app elevation="0">
      <v-container>
        <MenuBar
          class="desktop-menu"
          @openDialog="langDialog = true"
          @openLoginDialog="loginDialog = true"
        />
        <MobileMenu
          class="small-screen-menu"
          @openDialog="loginDialog = true"
          @openSideMenu="sideMenu = true"
        />
      </v-container>
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>

    <v-footer dark color="#000">
      <v-container>
        <AppFooter />
        <span class="mt-5 text-center caption"
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
    <SideMenu :class="{ active: sideMenu }" @closeSideMenu="sideMenu = false" />
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data() {
    return {
      langDialog: false,
      loginDialog: false,
      sideMenu: false,
    };
  },
  methods: {
    closeDialog() {
      this.langDialog = false;
    },
  },
};
</script>
<style scoped>
.small-screen-menu {
  display: none;
}
@media (max-width: 900px) {
  .desktop-menu {
    display: none;
  }
  .small-screen-menu {
    display: flex;
  }
}
@media (max-width: 500px) {
  span.mt-5.caption {
    display: block;
    text-align: center;
  }
}
</style>
