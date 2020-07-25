<template>
  <div class="home-intro-wrap">
    <div class="home-intro section relative">
      <b-container>
        <div class="home-intro__text-and-form-wrap">
          <div class="home-intro__text text-center">
            <div class="award relative">
              <Title small bold white title="بدا في عام 1994 م " />
              <div class="award__icon">
                <font-awesome-icon :icon="['fas', 'award']" />
              </div>
            </div>
            <Title big bold white title="الكحال " />
            <Title
              small
              bold
              white
              title="یمتلك نخبة من الإستشاریین و أساتذة الجامعة في كافة تخصصات طب و جراحة العیون"
            />
          </div>
          <div class="home-intro__form relative">
            <Form />
          </div>
        </div>

        <div class="bottom-svg">
          <svg
            class="divider--hills"
            viewBox="0 0 1920 105"
            xmlns="http://www.w3.org/2000/svg"
            preserveAspectRatio="none"
            role="img"
            aria-hidden="true"
            focusable="false"
          >
            <g fill-rule="evenodd" transform="matrix(1 0 0 -1 0 105)">
              <path
                d="m1920 14.8827052c-116.23325 0-224.05162 88.3906828-395.09265 88.3906828-160.92196 0-254.53172-83.4344997-444.90735-83.4344997-154.297581 0-240.095847 39.6344097-367.66819 39.6344097-154.121863 0-198.902329-36.1223133-349.458242-36.1223133-144.878137 0-241.175717 80.8685493-362.873568 80.8685493 0-34.0793243 0-68.1494291 0-102.219534h1920z"
              />
              <path
                d="m1920 14.6612844c-116.11434 0-223.9659 88.8291396-395.06196 88.8291396-160.92415 0-254.54487-83.7874573-444.93804-83.7874573-154.317311 0-240.088941 39.8974838-367.565152 39.8974838-154.034172 0-198.792715-36.4840402-349.164477-36.4840402-144.965828 0-241.283139 81.1250467-363.270371 81.1250467 0-34.7474052 0-69.4948104 0-104.241457h1920z"
              />
            </g>
          </svg>
        </div>
      </b-container>
    </div>
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
  background: linear-gradient(#0095af, #0095af);
  background-size: contain;
  background-position: right;
  background-repeat: no-repeat;
  height: 450px;
}

.home-intro__text-and-form-wrap {
  position: absolute;
  width: 50%;
  left: 50%;
  bottom: -50%;
  transform: translateX(-50%);
  z-index: 9;
}

.award__icon {
  position: absolute;
  opacity: 0.1;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.award__icon svg {
  font-size: 4rem;
  color: #fff;
}
</style>