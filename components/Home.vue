<template>
  <div class="home section">
    <div class="divider"></div>
    <div class="divider"></div>
    <b-container>
      <b-row>
        <b-col md="5" lg="6">
          <div class="home_img flex-center">
            <Title big bold title="الكحال" class="kahhal-name" />
            <Title medium bold sky title="خبراء طب العيون " />
            <Title
              small
              bold
              sky
              title="علی مدار ٣٥ عاماً ونحن نسعی دائماً لنكون اختياركم الآمن والأول لسلامة أعينكم"
            />
          </div>
        </b-col>

        <b-col md="7" lg="6">
          <div
            class="home__form relative"
            data-aos="fade-up"
            data-aos-offset="200"
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
  background-image: -webkit-gradient(
    linear,
    left bottom,
    left top,
    from(transparent),
    color-stop(90%, #11799a)
  );
  background-image: -o-linear-gradient(bottom, transparent, #11799a 90%);
  background-image: linear-gradient(0deg, transparent, #11799a 90%),
    url("../assets/images/video-1-e.png");
  background-size: 100% 100%;
  padding-bottom: 5rem;
}
</style>