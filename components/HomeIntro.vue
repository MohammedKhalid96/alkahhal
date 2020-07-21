<template>
  <div class="home-page">
    <div class="home-intro-section section relative">
      <b-container></b-container>

      <div class="top-shape">
        <b-img src="../assets/images/bg-top.png" fluid-grow></b-img>
      </div>
    </div>
    <div class="servies-section section">
      <Services />
    </div>
  </div>
</template>

<script>
import Title from "./Title";
import Form from "./Form";
import Services from "./Services";

export default {
  name: "HomeIntro",

  components: { Title, Form, Services }
};
</script>

<style scoped>
</style>