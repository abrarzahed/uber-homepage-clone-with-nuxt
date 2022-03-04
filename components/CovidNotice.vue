<template>
  <div class="covid-notice-box">
    <v-container v-if="showNotice">
      <div class="covid-notice-box-inner py-6">
        <h4>Helping to keep each other safe</h4>
        <p>
          We’re actively monitoring the COVID-19 situation and are continually
          working to help keep those who rely on our platform healthy and safe.
        </p>
        <a href="#">Go to Uber’s COVID-19 hub</a>
        <a href="#">Read about our Door-to-Door Safety Standard</a>
        <span @click="closeCovidNotice" class="font-weight-black">&times;</span>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showNotice: true,
    };
  },
  methods: {
    closeCovidNotice() {
      this.showNotice = false;
    },
  },
};
</script>

<style>
.covid-notice-box {
  background: #eff3fe;
}
.covid-notice-box-inner {
  display: grid;
  gap: 15px;
  position: relative;
}
.covid-notice-box-inner span {
  position: absolute;
  top: 0;
  right: 0;
  font-size: 28px;
  cursor: pointer;
}
.covid-notice-box-inner h4 {
  font-size: 18px;
  font-weight: 500;
  line-height: 1.5;
  margin: 0;
}
.covid-notice-box-inner p {
  font-size: 14px;
  line-height: 1.5;
  margin: 0;
}
.covid-notice-box-inner a {
  font-size: 14px;
  line-height: 1.5;
  margin: 0;
  color: inherit;
}
</style>
