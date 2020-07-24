<template>
  <div class="footer relative section">
    <div class="top-shape">
      <b-img src="../assets/images/top-1.png" fluid-grow></b-img>
    </div>
    <b-container>
      <b-row>
        <b-col md="3">
          <div class="footer__about">
            <div class="footer__about__logo">
              <b-img-lazy src="../assets/images/logo-white.png" fluid></b-img-lazy>
            </div>
            <div class="footer__about__info">
              <Title
                white
                small
                title="الكحال بدا في عام 1994 م یمتلك نخبة من الإستشاریین و أساتذة الجامعة في كافة تخصصات طب و جراحة العیون"
              />
            </div>
          </div>
        </b-col>

        <b-col md="3">
          <div class="footer__links">
            <a href="#">علاج اعتلال الشبكية السكرى والناتج عن مضاعفات مرض السكر</a>
            <a href="#">عمليات السائل الزجاجي وانفصال الشبكية لمرضي السكر</a>
            <a href="#">عمليات ازالة المياه البيضاء بتقنية الفاكو</a>
            <a href="#">عمليات المياه الزرقاء وعلاج ارتفاع ضغط العين</a>
            <a href="#">عمليات الليزك وتصحيح الابصار</a>
          </div>
        </b-col>

        <b-col md="3">
          <div class="footer__links">
            <a href="#">عملية زراعة العدسات لعلاج قصر او طول النظر</a>
            <a href="#">عمليات مرض حول العين عند الاطفال والكبار</a>
            <a href="#">عمليات انسداد المجرى الدمعى وجفاف العين لدى الكبار</a>
            <a href="#">عمليات تجميل الجفون</a>
          </div>
        </b-col>

        <b-col md="3">
          <div class="footer__contact">
            <ul>
              <li>
                <a :href="'tel:'+contactInfoHotLine">
                  <font-awesome-icon :icon="['fas', 'mobile-alt']" />
                  <span class="contact-info__name">الخط الساخن</span>
                  {{contactInfoHotLine}}
                </a>
              </li>
              <li>
                <a :href="'mailto:'+contactInfoEmail">
                  <font-awesome-icon :icon="['fas', 'envelope']" />
                  <span class="contact-info__name">البريد الألكتروني</span>
                  {{contactInfoEmail}}
                </a>
              </li>
              <li>
                <a
                  target="_blank"
                  href="https://www.google.com.eg/maps/place/%D9%85%D8%AC%D9%85%D8%B9+%D8%A7%D9%84%D9%83%D8%AD%D8%A7%D9%84+%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%E2%80%AD/@26.4737274,50.0957093,18z/data=!3m1!4b1!4m5!3m4!1s0x3e49fea90b63e9b5:0xa6d890753e9d119!8m2!3d26.4737274!4d50.094615"
                >
                  <font-awesome-icon :icon="['fas', 'map']" />
                  <span class="contact-info__name">فرع الدمام</span>
                  {{contactInfoAddressDammam}}
                </a>
              </li>

              <li>
                <a
                  target="_blank"
                  href="https://www.google.com.eg/maps/place/%D8%AA%D9%83%D9%86%D9%88+%D8%B9%D8%A7%D9%84%D9%85+%D8%A7%D9%84%D8%A5%D9%84%D9%83%D8%AA%D8%B1%D9%88%D9%86%D9%8A%D8%A7%D8%AA%E2%80%AD/@25.4344079,49.5729103,20.08z/data=!4m12!1m6!3m5!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!2z2KrZg9mG2Ygg2LnYp9mE2YUg2KfZhNil2YTZg9iq2LHZiNmG2YrYp9iq!8m2!3d25.4344162!4d49.5725679!3m4!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!8m2!3d25.4344162!4d49.5725679"
                >
                  <font-awesome-icon :icon="['fas', 'map']" />
                  <span class="contact-info__name">فرع الأحساء</span>
                  {{contactInfoAddressAlhesa}}
                </a>
              </li>
            </ul>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";

export default {
  name: "Footer",

  components: {
    Title,
  },
};
</script>

<style scoped>
.footer {
  background: #0096af;
}

.footer__about__logo img {
  width: 9rem;
}

.footer__links a {
  margin-bottom: 2rem;
  color: #fff;
}
</style>