<template>
  <div class="map">
    <b-container>
      <div class="dammam-branch">
        <b-row>
          <b-col md="6">
            <div class="map__img relative">
              <b-img-lazy src="../assets/images/map.jpg" fluid></b-img-lazy>
              <a
                target="_blank"
                href="https://www.google.com.eg/maps/place/%D9%85%D8%AC%D9%85%D8%B9+%D8%A7%D9%84%D9%83%D8%AD%D8%A7%D9%84+%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%E2%80%AD/@26.4737274,50.0957093,18z/data=!3m1!4b1!4m5!3m4!1s0x3e49fea90b63e9b5:0xa6d890753e9d119!8m2!3d26.4737274!4d50.094615"
              >
                <div class="map__img__overlay"></div>
              </a>
            </div>
          </b-col>

          <b-col md="6">
            <div class="map__img relative">
              <b-img-lazy src="../assets/images/map.jpg" fluid></b-img-lazy>
              <a
                target="_blank"
                href="https://www.google.com.eg/maps/place/%D9%85%D8%AC%D9%85%D8%B9+%D8%A7%D9%84%D9%83%D8%AD%D8%A7%D9%84+%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%E2%80%AD/@26.4737274,50.0957093,18z/data=!3m1!4b1!4m5!3m4!1s0x3e49fea90b63e9b5:0xa6d890753e9d119!8m2!3d26.4737274!4d50.094615"
              >
                <div class="map__img__overlay"></div>
              </a>
            </div>
          </b-col>
        </b-row>
      </div>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";

export default {
  name: "Map",

  components: { Title },

  data() {
    return {};
  },
};
</script>

<style scoped>
.map__img__overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: radial-gradient(closest-side, transparent, #fff 80%),
    url("../assets/images/pattern-2.png");
  background-size: cover;
}
</style>