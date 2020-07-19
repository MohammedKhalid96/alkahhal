<template>
  <div class="home-intro section relative">
    <b-container>
      <div class="home-intro__text">
        <Title white small title="بدا في عام 1994 م" />
        <Title white big bold title="الكحّال" />
        <Title
          white
          medium
          title="یمتلك نخبة من الإستشاریین و أساتذة الجامعة في كافة تخصصات طب و جراحة العیون"
        />
      </div>
    </b-container>
    <div class="top-shape">
      <b-img src="../assets/images/bg-top.png" fluid-grow></b-img>
    </div>
  </div>
</template>

<script>
import Title from "./Title";

export default {
  name: "HomeIntro",

  components: { Title }
};
</script>

<style scoped>
.home-intro {
  background: #0096af;
}

.home-intro__text {
  width: 50%;
}
</style>