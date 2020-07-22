<template>
  <div class="home-intro">
    <div class="home-intro-section section relative">
      <b-container></b-container>
    </div>
  </div>
</template>

<script>
import Title from "./Title";
import Form from "./Form";

export default {
  name: "HomeIntro",

  components: { Title, Form },
};
</script>

<style scoped>
.home-intro {
  height: 600px;
  background: url("../assets/images/pattern-8.png");
  background-size: contain;
  background-position: right;
  background-repeat: no-repeat;
}
</style>