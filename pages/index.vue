<template>
  <div class="home-page">
    <div id="home-intro" class="home-intro-section relative">
      <Home />
    </div>

    <div id="services" class="servies-section">
      <Services />
    </div>
    <div class="divider"></div>

    <div id="video" class="video-section">
      <Video />
    </div>
    <div class="divider"></div>

    <div id="doctors" class="doctors-section">
      <Doctors />
    </div>
    <div class="divider"></div>

    <div id="contact" class="contact-section">
      <Contact />
    </div>
  </div>
</template>

<script>
import Title from "../components/Title";
import Home from "../components/Home";
import Doctors from "../components/Doctors";
import Services from "../components/Services";
import Video from "../components/Video";
import Contact from "../components/Contact";

export default {
  name: "HomePage",

  components: {
    Home,
    Title,
    Doctors,
    Services,
    Video,
    Contact,
  },
};
</script>

<style scoped>
</style>