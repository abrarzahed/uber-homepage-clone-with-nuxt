<template>
  <div>
    <v-dialog v-model="dialog" fullscreen transition="dialog-top-transition">
      <v-card>
        <v-container>
          <div class="lang-dialog-box">
            <h2 class="section-title mb-16">Select your preferred language</h2>
            <v-btn class="capitalize-btn dark large-btn mr-10" depressed x-large
              >English</v-btn
            >
            <v-btn
              class="capitalize-btn dark large-btn"
              color="#fff"
              depressed
              x-large
              >বাংলা</v-btn
            >

            <div class="close-icon">
              <v-btn @click="close" depressed fab>
                <v-icon size="40">mdi-close</v-icon>
              </v-btn>
            </div>
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
      this.$emit("closeDialog");
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
</style>
