<template>
  <div class="thanks-wrap">
    <b-container>
      <div class="thanks flex-center text-center">
        <Title
          medium
          bold
          sky
          title="شكرا لتواصلك معنا سيتم التواصل معك من فريق خدمة العملاء لتأكيد الحجز"
        />
      </div>
    </b-container>
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
}
</style>

