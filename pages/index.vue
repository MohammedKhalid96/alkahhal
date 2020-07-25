<template>
  <div class="home-page">
    <div class="home-intro-section">
      <HomeIntro />
    </div>
    <div class="divider"></div>
    <div class="divider"></div>

    <div class="servies-section">
      <Services />
    </div>
    <div class="divider"></div>

    <div class="about-section">
      <About />
    </div>
    <div class="divider"></div>

    <div class="contact-section">
      <Contact />
    </div>
    <div class="divider"></div>
    <div class="map-section">
      <Map />
    </div>
    <div class="divider"></div>
    <div class="divider"></div>
  </div>
</template>

<script>
import Title from "../components/Title";
import HomeIntro from "../components/HomeIntro";
import Form from "../components/Form";
import Services from "../components/Services";
import About from "../components/About";
import Contact from "../components/Contact";
import Map from "../components/Map";

export default {
  name: "HomePage",

  components: {
    HomeIntro,
    Title,
    Form,
    Services,
    About,
    Contact,
    Map,
  },
};
</script>

<style scoped>
.servies-section,
.contact-section {
  background: url("../assets/images/right-bg.svg");
  background-position: top right;
  background-repeat: no-repeat;
  background-size: contain;
}

.about-section {
  background: url("../assets/images/left-bg.svg");
  background-position: top left;
  background-repeat: no-repeat;
  background-size: contain;
}
</style>