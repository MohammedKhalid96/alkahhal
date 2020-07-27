<template>
  <div class="home-page">
    <div id="home-intro" class="home-intro-section">
      <Home />
    </div>
    <div class="divider"></div>

    <div id="services" class="servies-section">
      <Services />
    </div>
    <div class="divider"></div>

    <div id="doctors" class="doctors-section">
      <Doctors />
    </div>
    <div class="divider"></div>

    <div id="about" class="about-section">
      <About />
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
import Form from "../components/Form";
import Doctors from "../components/Doctors";
import Services from "../components/Services";
import About from "../components/About";
import Contact from "../components/Contact";
import Counter from "../components/Counter";

export default {
  name: "HomePage",

  components: {
    Home,
    Title,
    Form,
    Doctors,
    Services,
    About,
    Contact,
    Counter,
  },
};
</script>

<style scoped>
/* .servies-section,
.contact-section {
  background: url("../assets/images/right-bg.svg");
  background-position: top right;
  background-repeat: no-repeat;
  background-size: contain;
}

.about-section,
.clients-section {
  background: url("../assets/images/left-bg.svg");
  background-position: top left;
  background-repeat: no-repeat;
  background-size: contain;
} */
</style>