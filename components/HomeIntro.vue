<template>
  <div class="home-page">
    <div class="home-intro-section section relative">
      <b-container></b-container>
    </div>
    <div class="servies-section">
      <Services />
    </div>

    <div class="contact-section">
      <Contact />
    </div>
  </div>
</template>

<script>
import Title from "./Title";
import Form from "./Form";
import Services from "./Services";
import Contact from "./Contact";

export default {
  name: "HomeIntro",

  components: { Title, Form, Services, Contact }
};
</script>

<style scoped>
.servies-section {
  background: url("../assets/images/right-bg.svg");
  background-position: top right;
  background-repeat: no-repeat;
}

.contact-section {
  background: url("../assets/images/left-bg.svg");
  background-position: top left;
  background-repeat: no-repeat;
}
</style>