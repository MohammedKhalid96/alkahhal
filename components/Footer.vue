<template>
  <div class="footer relative section">
    <div class="top-svg">
      <svg
        class="divider--hills"
        viewBox="0 0 1920 105"
        xmlns="http://www.w3.org/2000/svg"
        preserveAspectRatio="none"
        role="img"
        aria-hidden="true"
        focusable="false"
      >
        <g fill-rule="evenodd" transform="matrix(1 0 0 -1 0 105)">
          <path
            d="m1920 14.8827052c-116.23325 0-224.05162 88.3906828-395.09265 88.3906828-160.92196 0-254.53172-83.4344997-444.90735-83.4344997-154.297581 0-240.095847 39.6344097-367.66819 39.6344097-154.121863 0-198.902329-36.1223133-349.458242-36.1223133-144.878137 0-241.175717 80.8685493-362.873568 80.8685493 0-34.0793243 0-68.1494291 0-102.219534h1920z"
          />
          <path
            d="m1920 14.6612844c-116.11434 0-223.9659 88.8291396-395.06196 88.8291396-160.92415 0-254.54487-83.7874573-444.93804-83.7874573-154.317311 0-240.088941 39.8974838-367.565152 39.8974838-154.034172 0-198.792715-36.4840402-349.164477-36.4840402-144.965828 0-241.283139 81.1250467-363.270371 81.1250467 0-34.7474052 0-69.4948104 0-104.241457h1920z"
          />
        </g>
      </svg>
    </div>
    <div class="footer__form">
      <Form />
    </div>
    <div class="divider"></div>
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
          <div class="footer__contact footer__links">
            <li>
              <a :href="'tel:0553809777'">
                <div class="icon-img d-inline-block">
                  <b-img-lazy src="../assets/images/icons/phone-white.svg" fluid></b-img-lazy>
                </div>0553809777
              </a>
            </li>

            <li>
              <a :href="'mailto:alkahhalmedicalcomplex@gmail.com'">
                <div class="icon-img d-inline-block">
                  <b-img-lazy src="../assets/images/icons/mail-white.svg" fluid></b-img-lazy>
                </div>alkahhalmedicalcomplex@gmail.com
              </a>
            </li>

            <li>
              <a
                target="_blank"
                href="https://www.google.com.eg/maps/place/%D9%85%D8%AC%D9%85%D8%B9+%D8%A7%D9%84%D9%83%D8%AD%D8%A7%D9%84+%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%E2%80%AD/@26.4737274,50.0957093,18z/data=!3m1!4b1!4m5!3m4!1s0x3e49fea90b63e9b5:0xa6d890753e9d119!8m2!3d26.4737274!4d50.094615"
              >
                <div class="icon-img d-inline-block">
                  <b-img-lazy src="../assets/images/icons/location-white.svg" fluid></b-img-lazy>
                </div>7672 ابو قيس الجهني, حي الحمراء, الدمام, السعودية
              </a>
            </li>

            <li>
              <a
                target="_blank"
                href="https://www.google.com.eg/maps/place/%D8%AA%D9%83%D9%86%D9%88+%D8%B9%D8%A7%D9%84%D9%85+%D8%A7%D9%84%D8%A5%D9%84%D9%83%D8%AA%D8%B1%D9%88%D9%86%D9%8A%D8%A7%D8%AA%E2%80%AD/@25.4344079,49.5729103,20.08z/data=!4m12!1m6!3m5!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!2z2KrZg9mG2Ygg2LnYp9mE2YUg2KfZhNil2YTZg9iq2LHZiNmG2YrYp9iq!8m2!3d25.4344162!4d49.5725679!3m4!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!8m2!3d25.4344162!4d49.5725679"
              >
                <div class="icon-img d-inline-block">
                  <b-img-lazy src="../assets/images/icons/location-white.svg" fluid></b-img-lazy>
                </div>الأحساء, محاسن, المبرز
              </a>
            </li>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Form from "./Form";

export default {
  name: "Footer",

  components: {
    Title,
    Form,
  },
};
</script>

<style scoped>
.footer {
  background: #0096af;
}

.footer__about {
  margin-bottom: 5rem;
}

.footer__about__logo img {
  width: 9rem;
}

.footer__links a {
  margin-bottom: 2rem;
  color: #fff;
}

.footer__contact li {
  list-style: none;
}

.footer__links svg {
  margin-left: 0.5rem;
}

.icon-img {
  margin-left: 0.5rem;
  border-radius: 50%;
}

.icon-img img {
  width: 25px;
}

.footer__form {
  position: absolute;
  width: 50%;
  left: 50%;
  top: -65%;
  transform: translateX(-50%);
  z-index: 9;
}
</style>