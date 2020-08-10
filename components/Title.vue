<template>
  <div id="title">
    <h4
      class="title__element"
      :class="{
        title__big: big,
        title__medium: medium,
        title__small: small, 
        title__extra_small: extra_small,
        title__bold: bold, 
        title__white: white, 
        title__sky: sky, 
        title__gray: gray,
        title__shadow: shadow, 
        title__center: center
      }"
    >{{title}}</h4>
  </div>
</template>

<script>
export default {
  name: "Title",
  props: {
    title: String,
    big: Boolean,
    medium: Boolean,
    bold: Boolean,
    small: Boolean,
    extra_small: Boolean,
    white: Boolean,
    sky: Boolean,
    gray: Boolean,
    shadow: Boolean,
    center: Boolean,
  },
};
</script>

<style scoped>
#title {
  margin: 0.7rem 0;
}

.title__big {
  font-size: 3.3em;
  font-weight: bold;
}

.title__medium {
  font-size: 1.5em;
}

.title__small {
  font-size: 1.1em;
}

.title__extra_small {
  font-size: 0.9em;
}

.title__white {
  color: #fff;
}

.title__sky {
  color: #11799a;
}

.title__gray {
  color: #5c5d5e;
}

.title__bold {
  font-weight: bold;
}

.title__shadow {
  text-shadow: 0px 4px 8px rgba(0, 0, 0, 0.25);
}

.title__center {
  text-align: center;
}

@media (min-width: 992px) and (max-width: 1183px),
  screen and (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 320px) and (max-width: 767px) {
  .title__big {
    font-size: 2em;
  }
}
</style>