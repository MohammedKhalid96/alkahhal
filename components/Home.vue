<template>
  <div class="home section">
    <div class="divider"></div>

    <b-container>
      <b-row>
        <b-col md="5" lg="5">
          <div class="home_text">
            <Title bold sky title="الكحال" class="kahhal-name" />
            <Title medium bold gray title="خبراء طب العيون علی مدار ٣٥ عاماً " />
            <Title small gray title="ونحن نسعی دائماً لنكون اختياركم الآمن والأول لسلامة أعينكم" />
          </div>
        </b-col>

        <b-col md="7" lg="7"></b-col>
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
    height: 200px;
    -o-object-fit: cover;
    object-fit: cover;
    object-position: center;
  }

  .home_text {
    margin-bottom: 2rem;
  }
}
</style>