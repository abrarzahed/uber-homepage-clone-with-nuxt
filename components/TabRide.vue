<template>
  <div class="tab">
    <h3 class="text-h3 font-weight-medium">Request a ride now</h3>
    <div class="my-6 input-wrapper">
      <div class="line"></div>
      <v-text-field
        filled
        placeholder="Enter pickup location"
        append-icon="mdi-map-marker-radius"
        hide-details
        outlined
      ></v-text-field>
      <v-text-field
        filled
        placeholder="Enter destination"
        class="mt-3"
        hide-details
        outlined
      ></v-text-field>
    </div>
    <div class="button-link-group">
      <v-btn large tile dark color="#000" class="capitalize-btn"
        >Order now</v-btn
      >
      <v-btn large tile depressed class="capitalize-btn"
        >Schedule for later</v-btn
      >
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style>
.input-wrapper {
  position: relative;
}
.input-wrapper .line {
  position: absolute;
  width: 1px;
  height: 50px;
  background: #000;
  top: 35px;
  left: 25px;
}
.input-wrapper .line::before {
  content: "▭";
  position: absolute;
  top: -16px;
  left: -7px;
  font-size: 15px;
}
.input-wrapper .line::after {
  content: "▭";
  position: absolute;
  top: 43px;
  left: -7px;
  font-size: 15px;
}
.tab
  .theme--light.v-text-field--outlined:not(.v-input--is-focused):not(.v-input--has-state)
  > .v-input__control
  > .v-input__slot
  fieldset {
  border: none;
}

.tab
  .v-text-field.v-text-field--enclosed:not(.v-text-field--rounded)
  > .v-input__control
  > .v-input__slot,
.v-text-field.v-text-field--enclosed .v-text-field__details {
  padding: 0 12px;
  padding-left: 45px;
}
</style>
