<template>
  <div class="doctors-wrap section">
    <b-container>
      <div class="section-title text-center">
        <Title class="main-title" big bold title="الأطباء" />
        <Title
          small
          gray
          bold
          title="نمتلك نخبة من الإستشاریین و أساتذة الجامعة في كافة تخصصات طب و جراحة العیون"
        />
      </div>
      <b-row>
        <b-col v-for="owner in owners" :key="owner.id" md="3">
          <div class="owner">
            <div class="owner__box">
              <div class="owner__img relative">
                <b-img-lazy :src="owner.doctor_img" fluid-grow></b-img-lazy>
              </div>

              <div class="owner__info">
                <div class="owner__info__name">
                  <Title sky small bold :title="owner.doctor_name" />
                </div>

                <div class="owner__info__title">
                  <Title sky small bold :title="owner.doctor_title" />
                </div>
              </div>
            </div>
          </div>
        </b-col>

        <b-col md="9">
          <div class="doctors">
            <b-row>
              <b-col v-for="doctor in doctors" :key="doctor.id" md="4">
                <div class="doctors__box">
                  <div class="doctors__img relative">
                    <b-img-lazy :src="doctor.doctor_img" fluid-grow></b-img-lazy>
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
      owners: [
        {
          id: 1,
          doctor_img: require("../assets/images/doctors/د. عادل عبدالعزيز الرشود .jpeg"),
          doctor_name: "د. عادل عبدالعزيز الرشود ",
          doctor_title: "مؤسس شركة الكحال للخدمات الطبية",
          doctor_edu_one: "درجة الدكتوراه في طب وجراحة العيون.",
          doctor_edu_two: "زمالة جامعة الملك فيصل في طب وجراحة العيون.",
          doctor_edu_three: "عضو هيئة التدريس بجامعة الإمام عبدالرحمن بن فيصل.",
        },
      ],

      doctors: [
        {
          id: 2,
          doctor_img: require("../assets/images/doctors/عبدالعزيز عادل الرشود.jpg"),
          doctor_name: "د. عبد العزيز الرشود",
          doctor_title: "استشاري الشبكية والسائل الزجي والماء الابيض",
          doctor_edu_one: "درجة الدكتوراه في طب وجراحة العيون.",
          doctor_edu_two: "زمالة جامعة الملك فيصل في طب وجراحة العيون.",
          doctor_edu_three: "عضو هيئة التدريس بجامعة الإمام عبدالرحمن بن فيصل.",
        },
        {
          id: 3,
          doctor_img: require("../assets/images/doctors/عبدالرحمن الغديان.jpg"),
          doctor_name: "أ.د. عبد الرحمن الغديان",
          doctor_title: "استشاري الشبكية والسائل الزجاجي",
        },
        {
          id: 4,
          doctor_img: require("../assets/images/doctors/وقار مصفطي.jpg"),
          doctor_name: "د. وقار قريشي",
          doctor_title: "أخصائي طب وجراحة العيون",
        },
        {
          id: 5,
          doctor_img: require("../assets/images/doctors/محمد ضياء.jpeg"),
          doctor_name: "د. محمد ضياء الدين",
          doctor_title: "أخصائي عيون",
        },
        {
          id: 6,
          doctor_img: require("../assets/images/doctors/محمد النجار.jpg"),
          doctor_name: "د. محمد النجار",
          doctor_title: "أخصائي عيون",
        },

        {
          id: 7,
          doctor_img: require("../assets/images/eyes.png"),
          doctor_name: "د. الهام التميمي",
          doctor_title: "استشاري طب وجراحة العيون والحول للكبار والصغار",
        },
      ],
    };
  },
};
</script>

<style scoped>
.col-md-4 {
  margin-bottom: 3rem;
}

.col-md-4:nth-child(4),
.col-md-4:nth-child(5),
.col-md-4:nth-child(6) {
  margin-bottom: 0;
}

.col-md-3:nth-child(1) .owner__box::before,
.col-md-3:nth-child(1) .owner__box::after {
  position: absolute;
  content: "";
  width: 100%;
}

.col-md-3:nth-child(1) .owner__box::before {
  height: 200px;
  z-index: -2;
  top: -8vh;
  right: -6vh;
  bottom: 0;
  max-width: 65.7%;
  opacity: 1;
  background-image: -o-radial-gradient(#0096af 6%, transparent 0);
  background-image: radial-gradient(#0096af 6%, transparent 0);
  background-size: 35px 35px;
}

.col-md-3:nth-child(1) .owner__box::after {
  height: 150px;
  z-index: -3;
  top: -10vh;
  right: -1vh;
  bottom: 4vh;
  max-width: 227px;
  opacity: 0.7;
  background-image: -webkit-gradient(
    linear,
    right top,
    left top,
    from(#0096af),
    to(#0093ad80)
  );
  background-image: -o-linear-gradient(right, #0096af, #0093ad80);
  background-image: linear-gradient(to left, #0096af, #0093ad80);
}

.owner__box img {
  height: 610px;
  -o-object-fit: cover;
  object-fit: cover;
}

.doctors__img img {
  height: 240px;
}

.col-md-4:nth-child(6) img {
  -o-object-fit: contain;
  object-fit: contain;
}

.doctors__img::after {
  content: "";
  display: inline-block;
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-image: -webkit-gradient(
    linear,
    left bottom,
    left top,
    from(transparent),
    color-stop(90%, rgba(0, 149, 175, 0.15))
  );
  background-image: -o-linear-gradient(
    bottom,
    transparent,
    rgba(0, 149, 175, 0.15) 90%
  );
  background-image: linear-gradient(
    0deg,
    transparent,
    rgba(0, 149, 175, 0.15) 90%
  );
}

@media (min-width: 992px) and (max-width: 1183px) {
  .owner__box img {
    height: 454px;
  }
  .doctors__img img {
    height: 150px;
  }
  .col-md-3:nth-child(1) .owner__box::before {
    top: -3.5vh;
  }

  .col-md-3:nth-child(1) .owner__box::after {
    top: -4.5vh;
  }
}

@media (min-width: 768px) and (max-width: 991px) {
  .owner__box img {
    height: 440px;
  }
  .doctors__img img {
    height: 130px;
  }
  .col-md-3:nth-child(1) .owner__box::before {
    top: -3.5vh;
  }

  .col-md-3:nth-child(1) .owner__box::after {
    top: -4.5vh;
  }
}

@media (min-width: 320px) and (max-width: 767px) {
  .owner__box {
    margin-bottom: 3rem;
  }
  .owner__box img,
  .doctors__img img {
    height: auto;
  }

  .col-md-3:nth-child(1) .owner__box::before {
    top: -4.5vh;
  }

  .col-md-3:nth-child(1) .owner__box::after {
    top: -6vh;
  }

  .doctors__img img {
    height: auto;
  }

  .col-md-4:nth-child(4),
  .col-md-4:nth-child(5) {
    margin-bottom: 3rem;
  }
}
</style>