<template>
  <div class="app-add">
    <v-container>
      <h2 class="mb-10 section-title">There’s more to love in the apps</h2>
      <div class="app-add-container">
        <div class="app-add-card">
          <img src="~/assets/images/Driver-App-logo.png" alt="" />
          <h3>
            Download the driver app
            <span><v-icon color="#000">mdi-arrow-right</v-icon></span>
          </h3>
        </div>
        <div class="app-add-card">
          <img src="~/assets/images/Rider-App-logo.png" alt="" />
          <h3>
            Download the driver app
            <span><v-icon color="#000">mdi-arrow-right</v-icon></span>
          </h3>
        </div>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style>
.app-add {
  padding: 70px 0;
  background: #f6f6f6;
}
.app-add-container {
  display: flex;
  gap: 34px;
}
.app-add-card {
  display: flex;
  gap: 30px;
  align-items: center;
  padding: 30px;
  background: #fff;
  flex-basis: 50%;
  border: 1px solid #ddd;
}
.app-add-card h3 {
  font-size: 24px;
  font-weight: 500;
  letter-spacing: 0.5px;
  line-height: 32px;
  cursor: pointer;
}
.app-add-card h3 span {
  transition: all 0.2s;
}
.app-add-card h3:hover span {
  margin-left: 10px;
}
@media (max-width: 900px) {
  .app-add-container {
    flex-direction: column;
  }
}
@media (max-width: 500px) {
  .app-add-card {
    display: flex;
    gap: 30px;
    align-items: center;
    padding: 30px;
    background: #fff;
    flex-basis: 50%;
    border: 1px solid #ddd;
    flex-direction: column;
  }
}
</style>
