<template>
  <div class="footer-wrap">
    <!-- <div class="footer relative section">
      <b-container>
        <b-row>
          <b-col md="3">
            <div class="footer__about">
              <div class="footer__about__logo">
                <b-img-lazy src="../assets/images/logo.png" fluid></b-img-lazy>
              </div>
              <div class="footer__about__info">
                <Title
                  sky
                  small
                  bold
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
                    <b-img-lazy src="../assets/images/icons/phone.svg" fluid></b-img-lazy>
                  </div>0553809777
                </a>
              </li>

              <li>
                <a :href="'mailto:alkahhalmedicalcomplex@gmail.com'">
                  <div class="icon-img d-inline-block">
                    <b-img-lazy src="../assets/images/icons/mail.svg" fluid></b-img-lazy>
                  </div>alkahhalmedicalcomplex@gmail.com
                </a>
              </li>

              <li>
                <a
                  target="_blank"
                  href="https://www.google.com.eg/maps/place/%D9%85%D8%AC%D9%85%D8%B9+%D8%A7%D9%84%D9%83%D8%AD%D8%A7%D9%84+%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%E2%80%AD/@26.4737274,50.0957093,18z/data=!3m1!4b1!4m5!3m4!1s0x3e49fea90b63e9b5:0xa6d890753e9d119!8m2!3d26.4737274!4d50.094615"
                >
                  <div class="icon-img d-inline-block">
                    <b-img-lazy src="../assets/images/icons/location.svg" fluid></b-img-lazy>
                  </div>7672 ابو قيس الجهني, حي الحمراء, الدمام, السعودية
                </a>
              </li>

              <li>
                <a
                  target="_blank"
                  href="https://www.google.com.eg/maps/place/%D8%AA%D9%83%D9%86%D9%88+%D8%B9%D8%A7%D9%84%D9%85+%D8%A7%D9%84%D8%A5%D9%84%D9%83%D8%AA%D8%B1%D9%88%D9%86%D9%8A%D8%A7%D8%AA%E2%80%AD/@25.4344079,49.5729103,20.08z/data=!4m12!1m6!3m5!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!2z2KrZg9mG2Ygg2LnYp9mE2YUg2KfZhNil2YTZg9iq2LHZiNmG2YrYp9iq!8m2!3d25.4344162!4d49.5725679!3m4!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!8m2!3d25.4344162!4d49.5725679"
                >
                  <div class="icon-img d-inline-block">
                    <b-img-lazy src="../assets/images/icons/location.svg" fluid></b-img-lazy>
                  </div>الأحساء, محاسن, المبرز
                </a>
              </li>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>-->

    <div class="copyrights text-center">
      <div class="section-title text-center">
        <Title
          class="main-title"
          big
          bold
          title="لأنهم أملنا ومستقبلنا نهتم دائما بحماية ورعاية اعينهم"
        />
      </div>
      <Title sky small bold title="جميع الحقوق محفوظة الكحال" />
      <a target="_blank" href="https://jumppeak.net/">JUMPPEAK.</a>
    </div>
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
.footer-wrap {
  background-image: -webkit-gradient(
    linear,
    left bottom,
    left top,
    from(#0095af1c),
    to(transparent)
  );
  background-image: -o-linear-gradient(bottom, #0095af1c, transparent);
  background-image: linear-gradient(to top, #0095af1c, transparent);
}

.copyrights {
  padding-bottom: 0.5rem;
}

.copyrights a {
  color: #a9abad;
  font-weight: bold;
}
</style>