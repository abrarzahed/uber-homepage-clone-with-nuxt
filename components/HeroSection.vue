<template>
  <div class="hero-wrapper">
    <v-container>
      <div class="hero-section-content">
        <div class="hero-section-content-header" :class="activeTab">
          <div
            @click="handleActiveTab('drive')"
            class="hero-section-content-header-tab"
            :class="{ active: activeTab == 'drive' }"
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
            :class="{ active: activeTab == 'food' }"
          >
            <v-icon large color="#000">mdi-food-fork-drink</v-icon>
            <span>Eat</span>
          </div>
          <div
            @click="handleActiveTab('ride')"
            class="hero-section-content-header-tab"
            :class="{ active: activeTab == 'ride' }"
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
    <div class="hero-section" :class="activeTab"></div>
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
  margin-top: -30px;
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
  transform: translateX(50px);
}
.hero-section-content-header.food::before {
  transform: translateX(250px);
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
@media (max-width: 900px) {
  .hero-section-content {
    position: relative;
    top: 0;
    max-width: 100%;
  }
  .hero-section {
    min-height: 420px;
  }
  .hero-section-content-header {
    padding: 30px;
    justify-content: space-between;
  }
  .hero-section-content-tab-item {
    padding: 30px;
  }
  .hero-section-content-header.drive::before {
    transform: translateX(15px);
  }
  .hero-section-content-header.food::before {
    transform: translateX(330px);
  }
  .hero-section-content-header.ride::before {
    transform: translateX(800%);
  }
}
@media (max-width: 600px) {
  .hero-wrapper {
    margin-top: 0px;
  }
  .hero-section-content {
    position: relative;
    top: 0;
    max-width: 100%;
  }
  .hero-section {
    min-height: 380px;
  }
  .hero-section-content-header {
    gap: 0;
    padding: 20px;
    justify-content: space-between;
  }
  .hero-section-content-tab-item {
    padding: 20px 0px;
  }
  .hero-section-content-header::before {
    display: none;
  }
  .hero-section-content-header-tab.active span {
    color: #03235d;
    font-weight: 800;
    letter-spacing: 0.4px;
  }
}
</style>
