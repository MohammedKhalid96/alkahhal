<template>
  <div class="home-page">
    <div class="home-intro-section section relative">
      <b-container></b-container>
    </div>
    <div class="servies-section">
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