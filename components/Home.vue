<template>
  <div class="home section">
    <div class="divider"></div>
    <div class="divider"></div>
    <b-container>
      <b-row>
        <b-col>
          <div class="home_img flex-center">
            <Title small bold sky title="بدا في عام 1994 م " />
            <Title big bold sky title="الكحال " />
            <Title
              small
              bold
              sky
              title="یمتلك نخبة من الإستشاریین و أساتذة الجامعة في كافة تخصصات طب و جراحة العیون"
            />
          </div>
        </b-col>

        <b-col>
          <div
            class="home__form relative"
            data-aos="fade-up"
            data-aos-offset="200"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-easing="ease-in-out"
          >
            <Form />
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Form from "./Form";

export default {
  name: "Home",

  components: { Title, Form },
};
</script>

<style scoped>
.home {
  background-image: linear-gradient(0deg, transparent, #0095af1c 90%);
}

/* .home__form::after {
  position: absolute;
  width: 100%;
  content: "";
  z-index: -3;
  top: -10vh;
  right: 70px;
  bottom: 4vh;
  max-width: 427px;
  opacity: 1;
  background-image: linear-gradient(to left, #0096af, #0093ad80);
} */
</style>