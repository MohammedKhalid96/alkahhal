<template>
  <div class="about section">
    <b-container>
      <b-row>
        <b-col md="6">
          <div class="about-img">
            <b-img-lazy src="../assets/images/intro.png" fluid></b-img-lazy>
          </div>
        </b-col>

        <b-col md="6">
          <div class="about__info flex-center">
            <div class="section-title">
              <Title big bold title="عن الكحال" />
            </div>
            <Title
              sky
              small
              bold
              title="مراكز الكحّال الطبية هي الأولى والرائدة إقليميا و دوليا في تحقيق المعايير الطبية العالمية لجودة الرعاية الصحية المتكاملة للخدمات الطبية المؤيدة بالادلة من خلال فريق مهني متكامل ومحترف للمهارات العلمية والعملية على أحدث التقنيات التكنولوجية العالمية في التخصصات الطبية الدقيقة"
            />

            <Title
              sky
              small
              bold
              title="نعمل بحرفية عالية ودقة متناهية ومهارة مميزة على أحدث الاجهزة الطبية و أفضل الامكانيات الجراحية المتكاملة المدعومة بكل مايلزم من تقنيات عالمية مع توفر المستوى الرفيع من الخدمات الفندقية , تسهم جميعا في ضمان النتائج المرجوة من الاستشفاء وبلوغ ذروة الصحة والتعافي"
            />

            <div
              class="section-link"
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
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Button from "./Button";

export default {
  name: "About",

  components: { Title, Button },
};
</script>

<style scoped>
.about-img {
  background: url("../assets/images/circle.png");
  background-size: contain;
  padding: 3rem;
  padding-right: 0;
}

.about .section-title {
  margin: 0;
  text-align: right;
}

@media (min-width: 992px) and (max-width: 1183px) {
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 320px) and (max-width: 767px) {
  .about-img {
    background: none;
  }

  .about-img img {
    width: 100%;
  }
}
</style>