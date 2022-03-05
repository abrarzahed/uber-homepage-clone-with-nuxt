<template>
  <div>
    <v-dialog v-model="dialog" fullscreen transition="dialog-top-transition">
      <v-card>
        <v-container class="login-dialog">
          <div class="cta-container">
            <div class="cta-drive cta-item">
              <h2>Sign up to drive</h2>
              <span>
                <v-icon color="#000" size="50">mdi-arrow-right</v-icon>
              </span>
            </div>
            <div class="cta-ride cta-item">
              <h2>Sign up to drive</h2>
              <span>
                <v-icon size="50" color="#000">mdi-arrow-right</v-icon>
              </span>
            </div>
          </div>
          <div class="cta-drive cta-item outer">
            <h2>Sign in to order delivery with Uber Eats</h2>
            <span>
              <v-icon color="#000" size="50">mdi-arrow-right</v-icon>
            </span>
          </div>
          <div class="close-icon">
            <v-btn @click="close" depressed fab>
              <v-icon size="40">mdi-close</v-icon>
            </v-btn>
          </div>
        </v-container>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  props: {
    dialog: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {};
  },
  methods: {
    close() {
      this.$emit("closeSignInDialog");
    },
  },
};
</script>

<style>
.lang-dialog-box {
  padding: 150px 0;
  position: relative;
}
.lang-dialog-box .close-icon {
  position: absolute;
  top: 75px;
  right: 0;
}
.login-dialog {
  position: relative;
}
.login-dialog .close-icon {
  position: absolute;
  top: 70px;
  right: 0;
}
.login-dialog .cta-container {
  padding: 200px 0;
}
</style>
