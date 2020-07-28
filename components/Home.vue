<template>
  <div class="home section">
    <div class="divider"></div>
    <div class="divider"></div>
    <b-container>
      <b-row>
        <b-col md="5" lg="6">
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

        <b-col md="7" lg="6">
          <div
            class="home__form relative"
            data-aos="fade-up"
            data-aos-offset="200"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-easing="ease-in-out"
          >
            <Form />
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
  name: "Home",

  components: { Title, Form },
};
</script>

<style scoped>
.home {
  background-image: -webkit-gradient(linear, left bottom, left top, from(transparent), color-stop(90%, #0095af1c));
  background-image: -o-linear-gradient(bottom, transparent, #0095af1c 90%);
  background-image: linear-gradient(0deg, transparent, #0095af1c 90%);
}
</style>