<template>
  <div class="contact">
    <div class="section-title text-center">
      <Title class="main-title" big sky bold title="لا تجعل ضعف النظر يعيقك" />
    </div>

    <div class="contact__bg section">
      <b-container>
        <b-row>
          <b-col md="6">
            <Title medium center white bold title="  دائما بإنتظارك " />

            <div class="contact-info flex-center">
              <ul>
                <li>
                  <a :href="'tel:'+contactInfoHotLine">
                    <div class="contact-info__img d-inline-block">
                      <b-img-lazy src="../assets/images/icons/phone-white.svg" fluid></b-img-lazy>
                    </div>
                    <div class="contact-info__details d-inline-flex">
                      <p>
                        <span class="contact-info__name">الخط الساخن</span>
                        {{contactInfoHotLine}}
                      </p>
                    </div>
                  </a>
                </li>
                <li>
                  <a :href="'mailto:'+contactInfoEmail">
                    <div class="contact-info__img d-inline-block">
                      <b-img-lazy src="../assets/images/icons/mail-white.svg" fluid></b-img-lazy>
                    </div>
                    <div class="contact-info__details d-inline-flex">
                      <p>
                        <span class="contact-info__name">البريد الألكتروني</span>
                        {{contactInfoEmail}}
                      </p>
                    </div>
                  </a>
                </li>
                <li>
                  <a
                    target="_blank"
                    href="https://www.google.com.eg/maps/place/%D9%85%D8%AC%D9%85%D8%B9+%D8%A7%D9%84%D9%83%D8%AD%D8%A7%D9%84+%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%E2%80%AD/@26.4737274,50.0957093,18z/data=!3m1!4b1!4m5!3m4!1s0x3e49fea90b63e9b5:0xa6d890753e9d119!8m2!3d26.4737274!4d50.094615"
                  >
                    <div class="contact-info__img d-inline-block">
                      <b-img-lazy src="../assets/images/icons/location-white.svg" fluid></b-img-lazy>
                    </div>
                    <div class="contact-info__details d-inline-flex">
                      <p>
                        <span class="contact-info__name">فرع الدمام</span>
                        {{contactInfoAddressDammam}}
                      </p>
                    </div>
                  </a>
                </li>

                <li>
                  <a
                    target="_blank"
                    href="https://www.google.com.eg/maps/place/%D8%AA%D9%83%D9%86%D9%88+%D8%B9%D8%A7%D9%84%D9%85+%D8%A7%D9%84%D8%A5%D9%84%D9%83%D8%AA%D8%B1%D9%88%D9%86%D9%8A%D8%A7%D8%AA%E2%80%AD/@25.4344079,49.5729103,20.08z/data=!4m12!1m6!3m5!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!2z2KrZg9mG2Ygg2LnYp9mE2YUg2KfZhNil2YTZg9iq2LHZiNmG2YrYp9iq!8m2!3d25.4344162!4d49.5725679!3m4!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!8m2!3d25.4344162!4d49.5725679"
                  >
                    <div class="contact-info__img d-inline-block">
                      <b-img-lazy src="../assets/images/icons/location-white.svg" fluid></b-img-lazy>
                    </div>
                    <div class="contact-info__details d-inline-flex">
                      <p>
                        <span class="contact-info__name">فرع الأحساء</span>
                        {{contactInfoAddressAlhesa}}
                      </p>
                    </div>
                  </a>
                </li>
              </ul>
            </div>
          </b-col>

          <b-col md="6">
            <Title medium white center bold title="احجز الان لسلامة عينيك " />

            <div class="contact-form flex-center">
              <Form />
            </div>
          </b-col>
        </b-row>

        <div class="copyrights text-center">
          <Title white small bold title="جميع الحقوق محفوظة الكحال" />
          <a target="_blank" href="https://jumppeak.net/">JUMPPEAK.</a>
        </div>
      </b-container>
    </div>
  </div>
</template>

<script>
import Title from "./Title";
import Form from "./Form";

export default {
  name: "Contact",

  components: { Title, Form },

  data() {
    return {
      contactInfoHotLine: "0553809777",
      contactInfoEmail: "alkahhalmedicalcomplex@gmail.com",
      contactInfoAddressDammam: "7672 ابو قيس الجهني, حي الحمراء, الدمام, ",
      contactInfoAddressAlhesa: "الأحساء, محاسن, المبرز",
    };
  },
};
</script>

<style scoped>
.contact {
  background: url("../assets/images/little-eye.png");
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center left;
}

.contact__bg {
  background: rgba(0, 149, 175, 0.9);
}

.contact-info li {
  margin-bottom: 2rem;
}

.contact-info a {
  color: #fff;
  font-size: 1em;
}

.contact-info__img {
  width: 55px;
  height: 55px;
  line-height: 55px;
  text-align: center;
  margin-left: 1rem;
  border: 1px solid #fff;
  border-radius: 50%;
}

.contact-info__img img {
  width: 25px;
}

.contact-info__name {
  color: #5c5d5e;
  margin-left: 0.5rem;
}

.copyrights a {
  color: #fff;
}

@media (min-width: 992px) and (max-width: 1183px) {
  .contact-info__img {
    width: 30px;
    height: 30px;
    line-height: 30px;
    margin-left: 0rem;
  }

  .contact-info__img img {
    width: 20px;
  }

  .contact-info {
    font-size: 0.9rem;
  }
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 320px) and (max-width: 767px) {
  .contact-info__img {
    width: 20px;
    height: 20px;
    line-height: 20px;
    margin-left: 0rem;
  }

  .contact-info__img img {
    width: 15px;
  }

  .contact-info {
    font-size: 0.7rem;
  }

  .contact-info__img {
    display: none !important;
  }

  .contact-info__name {
    margin-left: 0.2em;
  }

  .contact-info li {
    margin-bottom: 1rem;
  }
}
</style>