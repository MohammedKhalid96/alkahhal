<template>
  <div class="home-page">
    <div id="home-intro" class="home-intro-section relative">
      <Home />
      <div class="bootom_svg">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
          <path
            fill="#117c9c1a"
            fill-opacity="1"
            d="M0,192L80,181.3C160,171,320,149,480,160C640,171,800,213,960,202.7C1120,192,1280,128,1360,96L1440,64L1440,0L1360,0C1280,0,1120,0,960,0C800,0,640,0,480,0C320,0,160,0,80,0L0,0Z"
          />
        </svg>
      </div>
    </div>

    <div id="services" class="servies-section">
      <Services />
    </div>
    <div class="divider"></div>

    <div id="doctors" class="doctors-section">
      <Doctors />
    </div>
    <div class="divider"></div>

    <div id="contact" class="contact-section">
      <Contact />
    </div>
    <div class="divider"></div>
  </div>
</template>

<script>
import Title from "../components/Title";
import Home from "../components/Home";
import Doctors from "../components/Doctors";
import Services from "../components/Services";
import About from "../components/About";
import Contact from "../components/Contact";

export default {
  name: "HomePage",

  components: {
    Home,
    Title,
    Doctors,
    Services,
    About,
    Contact,
  },
};
</script>

<style scoped>

</style>