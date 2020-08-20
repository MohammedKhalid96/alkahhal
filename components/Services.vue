<template>
  <div class="services relative pt-4 text-center">
    <b-container>
      <div class="service-section-title">
        <div class="section-title text-center">
          <Title class="main-title" big bold white title="خدماتنا لأمان عينيك " />
          <Title
            small
            white
            title="نحن نقدم لكم خدمات عالية الجودة في تخصص العيون بأفضل وأحدث الأجهزة المتطورة لأن هي الحفاظ على أعينكم دوماً"
          />
        </div>
      </div>

      <hooper :settings="hooperSettings" ref="carousel" @slide="updateCarousel">
        <slide v-for="service in services" :key="service.id">
          <div class="service-box">
            <div class="service-img">
              <b-img-lazy :src="service.service_img"></b-img-lazy>
            </div>

            <div>
              <Title small bold sky :title="service.service_name" class="service-name" />
            </div>

            <div class="service-action">
              <Button smallRadius transparent v-scroll-to="'#contact-form'">
                <font-awesome-icon :icon="['fas', 'calendar-check']" />احجز الآن
              </Button>
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
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Button from "./Button";

import { Hooper, Slide } from "hooper";
import "hooper/dist/hooper.css";

export default {
  name: "Services",

  components: {
    Title,
    Button,
    Hooper,
    Slide,
  },

  data() {
    return {
      services: [
        {
          id: 1,
          service_img: require("../assets/images/services/علاج اعتلال الشبكية السكرى والناتج عن مضاعفات مرض السكر.png"),
          service_name:
            "علاج اعتلال الشبكية السكرى والناتج عن مضاعفات مرض السكر",
        },
        {
          id: 2,
          service_img: require("../assets/images/services/عمليات السائل الزجاجى وانفصال الشبكية لمرضي السكر.jpg"),
          service_name: "عمليات السائل الزجاجي وانفصال الشبكية لمرضي السكر",
        },
        {
          id: 3,
          service_img: require("../assets/images/services/عمليات ازالة المياه البيضاء بتقنية الفاكو.jpg"),
          service_name: "عمليات ازالة المياه البيضاء بتقنية الفاكو",
        },
        {
          id: 4,
          service_img: require("../assets/images/services/عمليات المياه الزرقاء وعلاج ارتفاع ضغط العين.jpg"),
          service_name: "عمليات المياه الزرقاء وعلاج ارتفاع ضغط العين",
        },
        {
          id: 5,
          service_img: require("../assets/images/services/عمليات الليزك وتصحيح الابصار.png"),
          service_name: "عمليات الليزك وتصحيح الابصار",
        },
        {
          id: 6,
          service_img: require("../assets/images/services/عملية زراعة العدسات لعلاج قصر او طول النظر.png"),
          service_name: "عملية زراعة العدسات لعلاج قصر او طول النظر",
        },
        {
          id: 7,
          service_img: require("../assets/images/services/عمليات مرض حول العين عند الاطفال والكبار.jpg"),
          service_name: "عمليات مرض حول العين عند الاطفال والكبار",
        },
        {
          id: 8,
          service_img: require("../assets/images/services/عمليات انسداد المجرى الدمعى وجفاف العين لدى الكبار.jpg"),
          service_name: "عمليات انسداد المجرى الدمعى وجفاف العين لدى الكبار",
        },
        {
          id: 9,
          service_img: require("../assets/images/services/عمليات تجميل الجفون.jpg"),
          service_name: "عمليات تجميل الجفون",
        },
      ],

      hooperSettings: {
        itemsToShow: 1,
        infiniteScroll: true,
        wheelControl: false,
        breakpoints: {
          767: {
            itemsToShow: 3,
          },
        },
      },
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
.service-section-title {
  background: #11799a;
}

.section-title {
  background: url("../assets/images/small-eye.png");
  background-position: right;
  background-size: contain;
  background-repeat: no-repeat;
  padding-bottom: 2rem;
}

.service-box {
  padding: 0.5rem;
  margin: 0 0.5rem;
  border-radius: 2rem;
  -webkit-transition: all 0.1s;
  -o-transition: all 0.1s;
  transition: all 0.1s;
}

.service-img img {
  width: 100%;
  height: 260px;
  -o-object-fit: cover;
  object-fit: cover;
  border-radius: 2rem;
}

.service-name {
  padding: 1rem 0 0 0;
  overflow: hidden;
  -o-text-overflow: ellipsis;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 1;
}

.service-action {
  position: relative;
  bottom: -1000px;
  margin-bottom: 1rem;
}

.service-box:hover .service-action {
  bottom: 0;
  -webkit-transition: all 0.3s;
  -o-transition: all 0.3s;
  transition: all 0.3s;
}

.slider-btns {
  margin-top: 2rem;
}

@media (min-width: 992px) and (max-width: 1183px) {
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 320px) and (max-width: 767px) {
  .service-img img {
    height: 200px;
  }

  .service-name {
    overflow: unset;
  }
}
</style>