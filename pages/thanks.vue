<template>
  <div class="thanks-wrap">
    <div class="thanks flex-center text-center pl-4 pr-4">
      <Title
        big
        bold
        sky
        shadow
        title="شكرا لتواصلك معنا سيتم التواصل معك من فريق خدمة العملاء لتأكيد الحجز"
      />
    </div>
  </div>
</template>

<script>
import Title from "../components/Title";

export default {
  name: "Thanks",

  components: {
    Title,
  },
};
</script>

<style scoped>
.thanks {
  height: 100vh;
  width: 100%;
  background: linear-gradient(#fff, rgba(255, 255, 255, 0.4)),
    url("../assets/images/little-eye.png");
  background-size: cover;
}

.thanks-wrap {
  background: url("../assets/images/home.png");
  background-size: cover;
  background-position: top right;
}

@media (min-width: 320px) and (max-width: 767px) {
  .thanks-wrap {
    background-position: center;
  }
}
</style>

