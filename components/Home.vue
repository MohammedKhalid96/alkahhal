<template>
  <div class="home section">
    <div class="divider"></div>
    <div class="divider"></div>
    <b-container>
      <div class="home_text text-center">
        <Title big bold white title="الكحال" class="kahhal-name" />
        <Title medium bold white title="خبراء طب العيون " />
        <Title
          small
          bold
          white
          title="علی مدار ٣٥ عاماً ونحن نسعی دائماً لنكون اختياركم الآمن والأول لسلامة أعينكم"
        />
      </div>
      <b-row>
        <b-col md="5" lg="6">
          <div class="home_img">
            <b-img src="../assets/images/video-2.jpg" alt fluid></b-img>
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
    from(#117a9a1a),
    color-stop(90%, #11799a)
  );
  background-image: -o-linear-gradient(bottom, #117a9a1a, #11799a 90%);
  background-image: linear-gradient(0deg, #117a9a1a, #11799a 90%);
  background-size: 100% 100%;
  padding-bottom: 5rem;
}

.home_text {
  margin-bottom: 5rem;
}

.home_img img {
  border-radius: 5rem;
  height: 323.33px;
}

@media (min-width: 768px) and (max-width: 991px) {
}

@media (min-width: 320px) and (max-width: 767px) {
  .home_img img {
    height: auto;
  }

  .home_text {
    margin-bottom: 2rem;
  }
}
</style>