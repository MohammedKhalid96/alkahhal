<template>
  <div class="home-wrap">
    <div class="home">
      <div class="divider"></div>
      <div class="divider"></div>

      <b-container>
        <b-row>
          <b-col md="5" lg="5">
            <div class="home_text">
              <Title bold sky title="خبراء طب العيون علی مدار 35 عاماً " class="kahhal-name" />
              <Title
                medium
                bold
                gray
                title="و نسعی دائماً لنكون اختياركم الآمن والأول لسلامة أعينكم"
              />
            </div>
          </b-col>

          <b-col md="7" lg="7"></b-col>
        </b-row>
      </b-container>
    </div>

    <div @click="togglePopup" class="latest-offers-btn">
      <div class="latest-offers-btn__intern-wrap">
        <Title small sky bold title="عرض ما بعد العيد" />
        <div class="latest-offers-btn__img">
          <b-img src="../assets/images/icons/percentage.png"></b-img>
        </div>
      </div>
    </div>

    <div @click="closePopup" :class="isActive" class="latest-offers-popup">
      <div class="latest-offers-popup__internal-wrap">
        <div class="offers pt-4 pb-4 relative">
          <div class="offers-grid">
            <div class="popup-close text-left">
              <font-awesome-icon :icon="['fas', 'times']" />
            </div>
            <b-row>
              <b-col cols="6" md="4" v-for="offer in offers" :key="offer.id">
                <div class="offer text-center">
                  <Title small sky bold :title="offer.name" class="mb-4" />
                  <b-img-lazy :src="offer.offerImage" fluid class="mb-2"></b-img-lazy>
                  <Title small sky bold :title="offer.price" />
                </div>
              </b-col>
            </b-row>
          </div>

          <div class="popup-action text-center mt-4">
            <Button smallRadius bgSky border v-scroll-to="'#contact-form'">
              <font-awesome-icon :icon="['fas', 'calendar-check']" />احجز الأن
            </Button>
          </div>

          <div class="text-left pl-5 mt-2">
            <Title extra_small sky title="العروض مستمرة لمدة شهر واحد *" />
          </div>
        </div>
      </div>
    </div>

    <div class="whatsapp">
      <a target="_blank" href="https://api.whatsapp.com/send?phone=++9660553809777">
        <font-awesome-icon :icon="['fab', 'whatsapp']" />
      </a>
    </div>
  </div>
</template>

<script>
import Title from "./Title";
import Button from "./Button";

export default {
  name: "Home",

  components: { Title, Button },

  data() {
    return {
      offers: [
        {
          id: 1,
          name: "الليزك",
          offerImage: require("../assets/images/offers/lasik.png"),
          price: "فقط 3999",
          bounce: "+ 500 فحوصات",
        },
        {
          id: 2,
          name: "الماء الابيض",
          offerImage: require("../assets/images/offers/whitewater.png"),
          price: "فقط 5999",
          bounce: "+ 500 فحوصات",
        },
        {
          id: 3,
          name: "الكشف عن الشبكية لمرضي السكري",
          offerImage: require("../assets/images/offers/retina.png"),
          price: "فقط 99",
        },
      ],

      isActive: "",
      animation: "stop",
    };
  },

  methods: {
    togglePopup() {
      this.isActive = "true";
    },

    closePopup() {
      this.isActive = "";
    },
  },
};
</script>

<style scoped>
.home-wrap {
  background: url("../assets/images/home.png");
  background-size: cover;
  background-position: top right;
}

.home {
  background: url("../assets/images/little-eye-opacity.png");
  background-repeat: no-repeat;
  background-size: contain;
  background-position: left;
  padding-bottom: 5rem;
}

.home_text {
  margin-bottom: 5rem;
}

.home_img img {
  border-radius: 5rem;
  height: 323.33px;
}

.whatsapp {
  position: fixed;
  z-index: 999;
  left: 0;
  bottom: 36%;
  text-align: center;
}

.whatsapp a {
  display: inline-block;
  background: #fff;
  color: #11799a;
  width: 4rem;
  height: 4rem;
  line-height: 3.2rem;
  font-size: 2rem;
  border: 2px solid #11799a;
  border-left: 0;
  border-top-right-radius: 1rem;
  border-bottom-right-radius: 1rem;
}

.latest-offers-btn {
  position: fixed;
  z-index: 999;
  width: 15%;
  left: 0;
  bottom: 3rem;
  background: #fff;
  border: 6px solid #11799a;
  border-left: 0;
  border-top-right-radius: 2rem;
  border-bottom-right-radius: 2rem;

  cursor: pointer;
}

.latest-offers-btn__intern-wrap {
  border: 5px solid #f2c916;
  padding: 1rem 2rem;
  border-top-right-radius: 1.5rem;
  border-bottom-right-radius: 1.5rem;
  background: url("../assets/images/icons/offer.png");
  background-position: left;
  background-size: contain;
  border-left: 0;
}

.latest-offers-btn__img img {
  width: 80px;
  margin-top: 1rem;
  -webkit-animation: offer_animation 2s infinite;
  -moz-animation: offer_animation 2s infinite;
  -o-animation: offer_animation 2s infinite;
  animation: offer_animation 2s infinite;
}

.latest-offers-popup {
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0;
  left: -100%;
  z-index: 9999;
  background: rgb(0, 0, 0, 0.5);
}

.latest-offers-popup__internal-wrap {
  position: fixed;
  width: 80%;
  background: #fff;
  top: 50%;
  left: -100%;
  -webkit-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  border: 6px solid #11799a;
  border-radius: 2rem;
}

.offers {
  border: 5px solid #f2c916;
  border-radius: 1.5rem;
}

.latest-offers-popup__btn {
  position: absolute;
  width: 20%;
  overflow: visible;
  right: -5%;
  bottom: 0;
  background: #fff;
  border-radius: 2rem;
}

.latest-offers-popup__btn .latest-offers-btn__intern-wrap {
  border: 0;
}

.popup-close {
  width: 100%;
  padding-left: 3.5rem;
  display: block;
  margin-bottom: 1rem;
  cursor: pointer;
}

.popup-close svg {
  color: #fff;
  background: #11799a;
  width: 30px;
  height: 30px;
  padding: 0.1rem;
  border-radius: 50%;
}

.true {
  left: 0;
  -webkit-transition: all 0.5s;
  -o-transition: all 0.5s;
  transition: all 0.5s;
}

.true .latest-offers-popup__internal-wrap {
  left: 50%;
  -webkit-transition: all 0.5s;
  -o-transition: all 0.5s;
  transition: all 0.5s;
}

@media (min-width: 768px) and (max-width: 991px) {
  .latest-offers-btn__intern-wrap #title {
    display: none;
  }

  .latest-offers-btn__intern-wrap {
    padding: 0.2rem;
    text-align: center;
  }

  .home_text {
    margin-bottom: 1rem;
  }

  .offers img {
    width: 50px;
  }

  .latest-offers-popup__internal-wrap {
    width: 90%;
  }

  .popup-close {
    padding-left: 1.5rem;
  }
}

@media (min-width: 320px) and (max-width: 767px) {
  .home {
    padding-bottom: 0;
    padding-top: 2rem;
  }

  .info_slider .doctors__box {
    height: auto;
  }

  .whatsapp {
    bottom: 34%;
  }

  .whatsapp a {
    font-size: 1.5rem;
    width: 3rem;
    height: 3rem;
    line-height: 2.2rem;
    background: rgba(255, 255, 255, 0.6) !important;
  }

  .latest-offers-btn__img img {
    width: 28px;
  }

  .latest-offers-btn {
    bottom: 20%;
    width: 15%;
    background: rgba(255, 255, 255, 0.6) !important;
  }
  .latest-offers-btn__intern-wrap #title {
    display: none;
  }

  .latest-offers-btn__intern-wrap {
    padding: 0.2rem;
    text-align: center;
  }

  .home_text {
    margin-bottom: 1rem;
  }

  .offers img {
    width: 50px;
  }

  .latest-offers-popup__internal-wrap {
    width: 90%;
  }

  .col-6 {
    margin: auto;
  }

  .popup-close {
    padding-left: 1.5rem;
  }
}
</style>