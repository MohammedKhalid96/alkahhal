<template>
  <div class="home section">
    <div class="divider"></div>
    <div class="divider"></div>
    <b-container>
      <b-row>
        <b-col md="6">
          <div class="home_img flex-center">
            <Title big bold title="خبراء العيون" class="kahhal-name" />
            <Title small bold sky title="أكثر من 30 عاما في طب العبون" />
            <Title
              small
              bold
              sky
              title="نمتلك نخبة من الإستشاریین و أساتذة الجامعة في كافة تخصصات طب و جراحة العیون"
            />
          </div>
        </b-col>

        <b-col md="6">
          <div
            class="home__form relative"
            data-aos="fade-up"
            data-aos-offset="200"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-easing="ease-in-out"
          >
            <Form2 />
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Form2 from "./Form2";

export default {
  name: "Home",

  components: { Title, Form2 },
};
</script>

<style scoped>
.home {
  background-image: linear-gradient(0deg, transparent, #0095af1c 90%);
}

/* .home__form::after {
  position: absolute;
  width: 100%;
  content: "";
  z-index: -3;
  top: -10vh;
  right: 70px;
  bottom: 4vh;
  max-width: 427px;
  opacity: 1;
  background-image: linear-gradient(to left, #0096af, #0093ad80);
} */
</style>