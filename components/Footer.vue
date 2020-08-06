<template>
  <div class="footer-wrap relative">
    <div class="top__svg">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
        <path
          fill="#117c9c1a"
          fill-opacity="1"
          d="M0,192L80,181.3C160,171,320,149,480,160C640,171,800,213,960,202.7C1120,192,1280,128,1360,96L1440,64L1440,320L1360,320C1280,320,1120,320,960,320C800,320,640,320,480,320C320,320,160,320,80,320L0,320Z"
        />
      </svg>
    </div>
    <div class="copyrights text-center">
      <Title sky small bold title="جميع الحقوق محفوظة الكحال" />
      <a target="_blank" href="https://jumppeak.net/">JUMPPEAK.</a>
    </div>
  </div>
</template>

<script>
import Title from "./Title";
import Form from "./Form";

export default {
  name: "Footer",

  components: {
    Title,
    Form,
  },
};
</script>

<style scoped>
.footer-wrap {
  background-image: -webkit-gradient(
    linear,
    left bottom,
    left top,
    from(#117a9a1a),
    to(transparent)
  );
  background-image: -o-linear-gradient(bottom, #117a9a4b, #117a9a1a);
  background-image: linear-gradient(to top, #117a9a4b, #117a9a1a);
}

.copyrights {
  padding-bottom: 0.5rem;
}

.copyrights a {
  color: #5c5d5e;
  font-weight: bold;
}
</style>