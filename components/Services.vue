<template>
  <div class="services section text-center">
    <b-container>
      <b-row>
        <b-col v-for="service in services" :key="service.id" md="3">
          <div class="service-box">
            <div class="service-img">
              <b-img-lazy :src="service.service_img" fluid></b-img-lazy>
            </div>

            <div class="service-name">
              <Title small sky :title="service.service_name" />
            </div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";

export default {
  name: "Services",

  components: { Title },

  data() {
    return {
      services: [
        {
          id: 1,
          service_img: require("../assets/images/services/service-1.png"),
          service_name:
            "علاج اعتلال الشبكية السكرى والناتج عن مضاعفات مرض السكر"
        },
        {
          id: 2,
          service_img: require("../assets/images/services/service-2.png"),
          service_name: "عمليات السائل الزجاجي وانفصال الشبكية لمرضي السكر"
        },
        {
          id: 3,
          service_img: require("../assets/images/services/service-3.png"),
          service_name: "عمليات ازالة المياه البيضاء بتقنية الفاكو"
        },
        {
          id: 4,
          service_img: require("../assets/images/services/service-4.png"),
          service_name: "عمليات المياه الزرقاء وعلاج ارتفاع ضغط العين"
        },
        {
          id: 5,
          service_img: require("../assets/images/services/service-1.png"),
          service_name: "عمليات الليزك وتصحيح الابصار"
        },
        {
          id: 6,
          service_img: require("../assets/images/services/service-2.png"),
          service_name: "عملية زراعة العدسات لعلاج قصر او طول النظر"
        },
        {
          id: 7,
          service_img: require("../assets/images/services/service-3.png"),
          service_name: "عمليات مرض حول العين عند الاطفال والكبار"
        },
        {
          id: 8,
          service_img: require("../assets/images/services/service-4.png"),
          service_name: "عمليات انسداد المجرى الدمعى وجفاف العين لدى الكبار"
        },
        {
          id: 9,
          service_img: require("../assets/images/services/service-1.png"),
          service_name: "عمليات تجميل الجفون"
        }
      ]
    };
  }
};
</script>

<style scoped>
.services .col-md-3 {
  margin: auto;
  margin-bottom: 5rem;
}

.services .col-md-3:nth-child(9) {
  margin-bottom: 0;
}

.service-img img {
  width: 80%;
  margin: auto;
}

.service-name {
  padding: 0 2rem;
}
</style>