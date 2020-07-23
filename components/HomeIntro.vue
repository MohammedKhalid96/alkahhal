<template>
  <div class="home-intro-wrap">
    <b-container>
      <div class="home-intro section relative">
        <div class="home-intro__form">
          <div class="home-intro__text text-center">
            <Title small white title="بدا في عام 1994 م " />
            <Title big bold white title="الكحال " />
            <Title
              small
              white
              title="یمتلك نخبة من الإستشاریین و أساتذة الجامعة في كافة تخصصات طب و جراحة العیون"
            />
          </div>
          <Form />
        </div>
        <div class="bottom-shape">
          <b-img src="../assets/images/bottom-1.png" fluid-grow></b-img>
        </div>
      </div>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Form from "./Form";

export default {
  name: "HomeIntro",

  components: { Title, Form },
};
</script>

<style scoped>
.home-intro {
  background: linear-gradient(#0095af, #0095af),
    url("../assets/images/banner-bg-1.png");
  background-size: contain;
  background-position: right;
  background-repeat: no-repeat;
  height: 400px;
}

.home-intro__form {
  position: absolute;
  width: 50%;
  left: 50%;
  bottom: -50%;
  transform: translateX(-50%);
  z-index: 9;
}
</style>