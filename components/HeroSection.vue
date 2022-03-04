<template>
  <div class="hero-wrapper">
    <div class="hero-section" :class="activeTab"></div>
    <v-container>
      <div class="hero-section-content">
        <div class="hero-section-content-header" :class="activeTab">
          <div
            @click="handleActiveTab('drive')"
            class="hero-section-content-header-tab"
          >
            <v-icon large color="#000">mdi-network-strength-3</v-icon>
            <span
              >Drive or <br />
              deliver</span
            >
          </div>
          <div
            @click="handleActiveTab('food')"
            class="hero-section-content-header-tab"
          >
            <v-icon large color="#000">mdi-food-fork-drink</v-icon>
            <span>Eat</span>
          </div>
          <div
            @click="handleActiveTab('ride')"
            class="hero-section-content-header-tab"
          >
            <v-icon large color="#000">mdi-car</v-icon>
            <span>Ride</span>
          </div>
        </div>
        <div class="hero-section-content-tab-item">
          <TabDrive v-show="activeTab == 'drive'" />
          <TabFood v-show="activeTab == 'food'" />
          <TabRide v-show="activeTab == 'ride'" />
        </div>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeTab: "drive",
    };
  },
  methods: {
    handleActiveTab(tab) {
      this.activeTab = tab;
    },
  },
};
</script>

<style>
.hero-wrapper {
  position: relative;
  overflow: hidden;
}
.hero-section {
  overflow: hidden;
  min-height: 670px;
  max-height: 670px;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  transition: background 1s ease;
}
.hero-section.drive {
  background-image: url("~/assets/images/hero-section-img-1.png");
}
.hero-section.food {
  background-image: url("~/assets/images/hero-section-img-2.png");
}
.hero-section.ride {
  background-image: url("~/assets/images/hero-section-img-3.png");
}
.hero-section-content {
  position: absolute;
  top: 60px;
  background: #fff;
  max-width: 570px;
}
.hero-section-content-header {
  display: flex;
  gap: 150px;
  padding: 30px 50px;
  border-bottom: 1px solid #ddd;
  position: relative;
  align-items: center;
  justify-content: center;
}
.hero-section-content-header::before {
  content: "";
  position: absolute;
  height: 4px;
  width: 80px;
  background: #000;
  bottom: 0;
  left: 0;
  transition: transform 0.2s ease;
}
.hero-section-content-header.drive::before {
  transform: translateX(40px);
}
.hero-section-content-header.food::before {
  transform: translateX(230px);
}
.hero-section-content-header.ride::before {
  transform: translateX(410px);
}

.hero-section-content-header-tab {
  display: grid;
  gap: 10px;
  justify-items: center;
  cursor: pointer;
}
.hero-section-content-header-tab span {
  line-height: 1;
  align-self: end;
}
.hero-section-content-tab-item {
  padding: 50px;
}
</style>
