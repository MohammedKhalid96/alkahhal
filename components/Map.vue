<template>
  <div class="map">
    <b-container>
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
          <div class="map__working-hours relative flex-center">
            <li v-for="workingHour in workingHours" :key="workingHour.id">
              <p>
                <span>{{ workingHour.day }}</span>
                {{ workingHour.hours }}
              </p>
            </li>
            <div class="map__working-hours__overlay"></div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";

export default {
  name: "Map",

  components: { Title },

  data() {
    return {
      workingHours: [
        {
          id: 1,
          day: "السبت",
          hours: "8:30 صباحا الي 12:00 مساءا - 3:30 مساءا الي 9:30 مساءا",
        },
        {
          id: 2,
          day: "الأحد",
          hours: "8:30 صباحا الي 12:00 مساءا - 3:30 مساءا الي 9:30 مساءا",
        },
        {
          id: 3,
          day: "الأثنين",
          hours: "8:30 صباحا الي 12:00 مساءا - 3:30 مساءا الي 9:30 مساءا",
        },
        {
          id: 4,
          day: "الثلاثاء",
          hours: "8:30 صباحا الي 12:00 مساءا - 3:30 مساءا الي 9:30 مساءا",
        },
        {
          id: 5,
          day: "الأربعاء",
          hours: "8:30 صباحا الي 12:00 مساءا - 3:30 مساءا الي 9:30 مساءا",
        },
        {
          id: 6,
          day: "الخميس",
          hours: "8:30 صباحا الي 12:00 مساءا - 3:30 مساءا الي 9:30 مساءا",
        },
        {
          id: 7,
          day: "الجمعة",
          hours: "8:30 صباحا الي 12:00 مساءا - 3:30 مساءا الي 9:30 مساءا",
        },
      ],
    };
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
  background: radial-gradient(closest-side, transparent, #fff 90%),
    url("../assets/images/map.jpg");
  background-size: contain;
}

.map__working-hours {
  padding: 6rem 7rem;
  background: url("../assets/images/circle-bg.png");
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
  border-radius: 10rem;
  list-style: none;
  color: #fff;
  font-weight: bold;
}

.map__working-hours__overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  background: url("../assets/images/circle.png");
  background-size: contain;
  background-repeat: no-repeat;
  z-index: -1;
}

.map__working-hours li {
    margin-bottom: 1.5rem;
}
</style>