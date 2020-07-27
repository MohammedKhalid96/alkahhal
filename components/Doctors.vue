<template>
  <div class="doctors section">
    <b-container>
      <b-row>
        <b-col v-for="doctor in doctors" :key="doctor.id" md="4" lg="3">
          <div class="doctors__box">
            <div class="doctors__img relative">
              <b-img-lazy :src="doctor.doctor_img" fluid></b-img-lazy>
            </div>

            <div class="doctors__info">
              <div class="doctor__info__name">
                <Title sky small bold :title="doctor.doctor_name" />
              </div>

              <div class="doctor__info__title">
                <Title sky small bold :title="doctor.doctor_title" />
              </div>
            </div>
          </div>
        </b-col>
      </b-row>

      <div
        class="section-link text-center"
        data-aos="fade-up"
        data-aos-offset="200"
        data-aos-delay="50"
        data-aos-duration="1000"
        data-aos-easing="ease-in-out"
      >
        <Button smallRadius bgSky v-scroll-to="'#contact'">
          <font-awesome-icon :icon="['fas', 'paper-plane']" />احجز موعد
        </Button>
      </div>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Button from "./Button";

export default {
  name: "Doctors",

  components: { Title, Button },

  data() {
    return {
      doctors: [
        {
          id: 1,
          doctor_img: require("../assets/images/doctors/عبدالعزيز عادل الرشود.jpg"),
          doctor_name: "د. عبد العزيز الرشود",
          doctor_title: "استشاري الشبكية والسائل الزجي والماء الابيض",
          doctor_edu_one: "درجة الدكتوراه في طب وجراحة العيون.",
          doctor_edu_two: "زمالة جامعة الملك فيصل في طب وجراحة العيون.",
          doctor_edu_three: "عضو هيئة التدريس بجامعة الإمام عبدالرحمن بن فيصل.",
        },
        {
          id: 2,
          doctor_img: require("../assets/images/doctors/وقار مصفطي.jpg"),
          doctor_name: "د. وقار قريشي",
          doctor_title: "أخصائي طب وجراحة العيون",
        },
        {
          id: 3,
          doctor_img: require("../assets/images/doctors/محمد ضياء.jpeg"),
          doctor_name: "د. محمد ضياء الدين",
          doctor_title: "أخصائي عيون",
        },
        {
          id: 4,
          doctor_img: require("../assets/images/doctors/محمد النجار.jpg"),
          doctor_name: "د. محمد النجار",
          doctor_title: "أخصائي عيون",
        },
      ],
    };
  },
};
</script>

<style scoped>
.col-md-4 {
}

.col-md-4:nth-child(1) .doctors__box::before,
.col-md-4:nth-child(1) .doctors__box::after {
  position: absolute;
  content: "";
  width: 100%;
}

.col-md-4:nth-child(1) .doctors__box::before {
  height: 200px;
  z-index: -2;
  top: -8vh;
  right: -6vh;
  bottom: 0;
  max-width: 65.7%;
  opacity: 1;
  background-image: radial-gradient(#0096af 6%, transparent 0);
  background-size: 35px 35px;
}

.col-md-4:nth-child(1) .doctors__box::after {
  height: 150px;
  z-index: -3;
  top: -10vh;
  right: -1vh;
  bottom: 4vh;
  max-width: 227px;
  opacity: 0.7;
  background-image: linear-gradient(to left, #0096af, #0093ad80);
}

.doctors__img img {
  height: 234px;
}

.doctors__img::after {
  content: "";
  display: inline-block;
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-image: linear-gradient(
    0deg,
    transparent,
    rgba(0, 149, 175, 0.15) 90%
  );
}
</style>