<template>
  <div class="footer">
    <div class="top-part">
      <h3 class="logo">Uber</h3>
      <p>Bangladesh ride sharing related information</p>
    </div>
    <p class="mt-6 mb-8">Visit Help Center</p>
    <v-row dense>
      <v-col cols="12" md="3">
        <h6 class="text-h6 mb-5">Company</h6>
        <p>About us</p>
        <p>Our offering</p>
        <p>Our Newsroom</p>
        <p>Inventors</p>
        <p>Blog</p>
        <p>Careers</p>
      </v-col>
      <v-col cols="12" md="3">
        <h6 class="text-h6 mb-5">Products</h6>
        <p>Ride</p>
        <p>Drive</p>
        <p>Deliver</p>
        <p>Eat</p>
        <p>Uber for business</p>
      </v-col>
      <v-col cols="12" md="3">
        <h6 class="text-h6 mb-5">Global citizenship</h6>
        <p>Safety</p>
        <p>Diversity and inclusion</p>
      </v-col>
      <v-col cols="12" md="3">
        <h6 class="text-h6 mb-5">Travel</h6>
        <p>Airports</p>
      </v-col>
    </v-row>
    <div class="footer-social mt-10">
      <div class="footer-icons">
        <v-btn text depressed dark>
          <v-icon>mdi-facebook</v-icon>
        </v-btn>
        <v-btn text depressed dark>
          <v-icon>mdi-twitter</v-icon>
        </v-btn>
        <v-btn text depressed dark>
          <v-icon>mdi-youtube</v-icon>
        </v-btn>
        <v-btn text depressed dark>
          <v-icon>mdi-linkedin</v-icon>
        </v-btn>
        <v-btn text depressed dark>
          <v-icon>mdi-instagram</v-icon>
        </v-btn>
        <v-btn class="capitalize-btn" text depressed dark>
          <v-icon left>mdi-web</v-icon>English
        </v-btn>
      </div>
      <div class="footer-app-icons">
        <img src="~/assets/images/play-store.svg" alt="" />
        <img src="~/assets/images/app-store.svg" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.footer {
  padding: 70px 0 20px;
}
.footer .top-part {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.footer-social {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.footer-social img {
  max-width: 120px;
  cursor: pointer;
}
.footer-icons {
  flex-basis: 50%;
}
.footer-app-icons {
  display: flex;
  flex-basis: 50%;
  margin-left: auto;
  justify-content: flex-end;
  align-items: center;
  gap: 10px;
}
@media (max-width: 500px) {
  .footer {
    padding: 30px 0 20px;
  }
  .footer .top-part {
    gap: 10px;
    align-items: flex-start;
    flex-direction: column;
  }
  .footer-social {
    flex-direction: column;
  }
  .footer-social img {
    width: 100%;
    display: inline-block;
    cursor: pointer;
  }
  .footer-icons {
    flex-basis: 100%;
    display: flex;
    /* padding: 20px; */
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 30px;
  }
  .footer-app-icons {
    flex-basis: 100%;
    margin-left: 0;
    justify-content: flex-end;
  }
}
</style>
