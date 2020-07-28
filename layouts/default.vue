<template>
  <div>
    <Nav2 />
    <nuxt />
    <Footer />
  </div>
</template>

<script>
import Nav2 from "../components/Nav2";
import Footer from "../components/Footer";

export default {
  components: {
    Nav2,
    Footer
  }
};
</script>
