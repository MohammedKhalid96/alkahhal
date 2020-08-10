<template>
  <div class="services relative text-center">
    <div class="section-title text-center">
      <Title class="main-title" big bold white title="خدماتنا لأمان عينيك " />
      <Title
        small
        white
        bold
        title="نحن نقدم لكم خدمات عالية الجودة في تخصص العيون بأفضل وأحدث الأجهزة المتطورة لأن هي الحفاظ على أعينكم دوماً"
      />
    </div>
    <b-container>
      <b-row>
        <client-only placeholder="Loading...">
          <agile :rtl="true" :infinite="true" :slidesToShow="5" :dots="false">
            <div v-for="service in services" :key="service.id">
              <div class="service-box">
                <div class="service-img">
                  <b-img-lazy :src="service.service_img" fluid></b-img-lazy>
                </div>

                <div class="service-name">
                  <Title small bold white :title="service.service_name" />
                </div>
              </div>
            </div>
          </agile>
        </client-only>
      </b-row>

      <div
        class="section-link"
        data-aos="fade-up"
        data-aos-duration="1000"
        data-aos-easing="ease-in-out"
      >
        <Button smallRadius bgSky v-scroll-to="'#contact'">
          <font-awesome-icon :icon="['fas', 'paper-plane']" />لغد أوضح احجز الآن
        </Button>
      </div>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Button from "./Button";

export default {
  name: "Services",

  components: { Title, Button },

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
          service_img: require("../assets/images/services/عمليات السائل الزجاجى وانفصال الشبكية لمرضي السكر.png"),
          service_name: "عمليات السائل الزجاجي وانفصال الشبكية لمرضي السكر",
        },
        {
          id: 3,
          service_img: require("../assets/images/services/عمليات ازالة المياه البيضاء بتقنية الفاكو.png"),
          service_name: "عمليات ازالة المياه البيضاء بتقنية الفاكو",
        },
        {
          id: 4,
          service_img: require("../assets/images/services/عمليات المياه الزرقاء وعلاج ارتفاع ضغط العين.png"),
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
          service_img: require("../assets/images/services/عمليات مرض حول العين عند الاطفال والكبار.png"),
          service_name: "عمليات مرض حول العين عند الاطفال والكبار",
        },
        {
          id: 8,
          service_img: require("../assets/images/services/عمليات انسداد المجرى الدمعى وجفاف العين لدى الكبار.png"),
          service_name: "عمليات انسداد المجرى الدمعى وجفاف العين لدى الكبار",
        },
        {
          id: 9,
          service_img: require("../assets/images/services/عمليات تجميل الجفون.png"),
          service_name: "عمليات تجميل الجفون",
        },
      ],
    };
  },
};
</script>

<style scoped>
.section-title {
  background: #11799a;
}

.service-img img {
}

.service-name {
  padding: 3rem 1rem;
  background: #0096af;
}

@media (min-width: 992px) and (max-width: 1183px) {
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 320px) and (max-width: 767px) {
}
</style>