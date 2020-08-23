<template>
  <div class="doctors-wrap section">
    <b-container>
      <div class="section-title text-center">
        <Title class="main-title" big sky bold title="نخبة من الاستشاريين وأساتذة الجامعة" />
        <Title small sky bold title="في كافة تخصصات طب وجراحة العيون" />
      </div>
      <b-row no-gutters>
        <b-col md="3">
          <hooper
            :settings="info_slider"
            class="info_slider"
            group="doctors_slider"
            ref="carousel"
            @slide="updateCarousel"
          >
            <slide v-for="doctor in doctors" :key="doctor.id">
              <div class="doctors">
                <div class="doctors__box">
                  <div class="doctors__info">
                    <div class="doctor__info__name">
                      <Title sky extra_small bold :title="doctor.doctor_name" />
                    </div>

                    <div class="doctor__info__title">
                      <Title sky extra_small bold :title="doctor.doctor_title" />
                    </div>
                  </div>
                </div>
              </div>
            </slide>
          </hooper>
          <div class="slider-btns">
            التالي
            <button @click.prevent="slidePrev" class="prev">
              <font-awesome-icon :icon="['fas', 'caret-right']" />
            </button>
            <button @click.prevent="slideNext" class="next">
              <font-awesome-icon :icon="['fas', 'caret-left']" />
            </button>
          </div>
        </b-col>

        <b-col md="9" class="img_slider_wrap">
          <hooper :settings="img_slider" group="doctors_slider" class="img_slider">
            <slide v-for="doctor in doctors" :key="doctor.id">
              <div class="doctors">
                <div class="doctors__box">
                  <div class="doctors__box__img">
                    <b-img-lazy :src="doctor.doctor_img" fluid></b-img-lazy>
                  </div>
                  <div class="doctors__info">
                    <div class="doctor__info__name text-center">
                      <Title sky extra_small bold :title="doctor.doctor_name" />
                    </div>
                  </div>
                </div>
              </div>
            </slide>
          </hooper>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Button from "./Button";

import { Hooper, Slide } from "hooper";
import "hooper/dist/hooper.css";

export default {
  name: "Doctors",

  components: {
    Title,
    Button,
    Hooper,
    Slide,
  },

  data() {
    return {
      owners: [
        {
          id: 1,
          doctor_img: require("../assets/images/doctors/د. عادل عبدالعزيز الرشود.png"),
          doctor_name: "د. عادل عبدالعزيز الرشود ",
          doctor_title:
            "مؤسس شركة الكحال للخدمات الطبیة واستشاري القرنية والماء الأبيض وتصحيح عیوب النظر الانكسارية",
          doctor_edu_one: "درجة الدكتوراه في طب وجراحة العيون.",
          doctor_edu_two: "زمالة جامعة الملك فيصل في طب وجراحة العيون.",
          doctor_edu_three: "عضو هيئة التدريس بجامعة الإمام عبدالرحمن بن فيصل.",
        },
      ],

      doctors: [
        {
          id: 1,
          doctor_img: require("../assets/images/new-doctors/د. عادل عبدالعزيز الرشود.jpg"),
          doctor_name: "د. عادل عبدالعزيز الرشود ",
          doctor_title:
            "مؤسس شركة الكحال للخدمات الطبیة واستشاري القرنية والماء الأبيض وتصحيح عیوب النظر الانكسارية",
        },
        {
          id: 3,
          doctor_img: require("../assets/images/new-doctors/عبدالرحمن الغديان.jpeg"),
          doctor_name: "أ.د. عبد الرحمن الغديان",
          doctor_title: "استشاري الشبكية والسائل الزجاجي",
        },
        {
          id: 4,
          doctor_img: require("../assets/images/new-doctors/ladies-doctors.jpg"),
          doctor_name: "د. الهام التميمي",
          doctor_title: "استشاري طب وجراحة العیون في الحول للأطفال والبالغين",
        },
        {
          id: 5,
          doctor_img: require("../assets/images/new-doctors/ladies-doctors.jpg"),
          doctor_name: "د. سناء عبد الكريم",
          doctor_title: "استشاري طب وجراحة العيون - الشبكية",
        },
        {
          id: 2,
          doctor_img: require("../assets/images/new-doctors/عبدالعزيز عادل الرشود.jpeg"),
          doctor_name: "د. عبد العزيز الرشود",
          doctor_title: "استشاري الشبكية والسائل الزجاجي والماء الأبيض",
        },
        {
          id: 6,
          doctor_img: require("../assets/images/new-doctors/محمد ضياء.jpeg"),
          doctor_name: "د. محمد ضياء الدين",
          doctor_title: "اخصائي طب وجراحة العيون",
        },
        {
          id: 8,
          doctor_img: require("../assets/images/new-doctors/محمد النجار.jpeg"),
          doctor_name: "د. محمد النجار",
          doctor_title: "اخصائي طب وجراحة العيون",
        },
        {
          id: 7,
          doctor_img: require("../assets/images/new-doctors/وقار مصفطي.jpeg"),
          doctor_name: "د. وقار قريشي",
          doctor_title: "أخصائي طب وجراحة العيون",
        },
        {
          id: 9,
          doctor_img: require("../assets/images/new-doctors/ladies-doctors.jpg"),
          doctor_name: "د. ليمياء فاروق",
          doctor_title: "أخصائية طب وجراحة العيون",
        },
        {
          id: 10,
          doctor_img: require("../assets/images/new-doctors/ladies-doctors.jpg"),
          doctor_name: "د. سارة سامي",
          doctor_title: "أخصائية طب وجراحة العيون",
        },
      ],

      info_slider: {
        itemsToShow: 1,
        infiniteScroll: true,
        wheelControl: false,
        breakpoints: {
          991: {
            itemsToShow: 1,
          },
        },
      },

      img_slider: {
        itemsToShow: 1,
        infiniteScroll: true,
        wheelControl: false,
        breakpoints: {
          991: {
            itemsToShow: 3,
          },
        },
      },

      carouselData: 0,
    };
  },
  watch: {
    carouselData() {
      this.$refs.carousel.slideTo(this.carouselData);
    },
  },

  methods: {
    slidePrev() {
      this.$refs.carousel.slidePrev();
    },
    slideNext() {
      this.$refs.carousel.slideNext();
    },
    updateCarousel(payload) {
      this.myCarouselData = payload.currentSlide;
    },
  },
};
</script>

<style scoped>
.doctors-wrap {
  background: url("../assets/images/Group 39.png");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: left;
}

.info_slider .doctors__box {
  height: 240px;
}

.info_slider .doctors__info {
  position: relative;
  top: 100%;
}

.img_slider_wrap .doctors__box {
  margin-left: 2rem;
}

.doctors__box__img img {
  height: 380px;
  object-fit: cover;
}
@media (min-width: 992px) and (max-width: 1183px) {
  .img_slider_wrap .doctors__box {
    margin-right: 2rem;
    margin-left: 0;
  }
}

@media (min-width: 768px) and (max-width: 991px) {
  .img_slider_wrap .doctors__box {
    margin-right: 2rem;
  }
}

@media (min-width: 320px) and (max-width: 767px) {
  .info_slider .doctors__box {
    height: auto;
  }

  .img_slider_wrap {
    margin-top: 5rem;
  }

  .img_slider_wrap .doctors__box {
    margin-left: 0;
  }
}
</style>