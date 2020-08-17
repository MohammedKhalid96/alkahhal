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

    <div id="doctors" class="doctors-section">
      <Doctors />
    </div>

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
#doctors {
  background-image: -o-linear-gradient(
    bottom,
    rgba(17, 124, 156, 0.2),
    rgba(17, 122, 154, 0.2)
  );
  background-image: -webkit-gradient(
    linear,
    left bottom,
    left top,
    from(rgba(17, 124, 156, 0.2)),
    to(rgba(17, 122, 154, 0.2))
  );
  background-image: linear-gradient(
    to top,
    rgba(17, 124, 156, 0.2),
    rgba(17, 122, 154, 0.2)
  );
}

#contact {
  background: rgba(17, 124, 156, 0.2);
}
</style>