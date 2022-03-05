<template>
  <div class="cta">
    <v-container>
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
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style>
.cta {
  padding: 70px 0;
}
.cta-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
}
.cta-item {
  padding-bottom: 20px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-basis: 50%;
  overflow: hidden;
  border-bottom: 1px solid #000;
  cursor: pointer;
}
.cta-item h2 {
  font-size: 36px;
  font-weight: 500;
}
.cta-item span {
  width: 40px;
  overflow: hidden;
}
.cta-item:hover span * {
  animation: hov 0.4s linear;
}
@keyframes hov {
  0% {
    transform: translateX(-100%);
    opacity: 0.1;
  }

  100% {
    transform: translateX(0);
    opacity: 1;
  }
}
@media (max-width: 900px) {
  .cta-container {
    align-items: stretch;
    justify-content: center;
    flex-direction: column;
  }
}
@media (max-width: 900px) {
  .cta-container h2 {
    font-size: 26px;
  }
  .cta-drive.cta-item.outer {
    display: none;
  }
}
</style>
