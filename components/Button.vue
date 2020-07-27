<template>
  <b-button
    class="button__element"
    :to="to"
    :block="block"
    :disabled="disabled"
    :type="type"
    :class="{fakelink__roundedradius: roundedRadius, fakelink__smallradius: smallRadius, dark: dark, sky: bgSky}"
  >
    <slot>{{content}}</slot>
  </b-button>
</template>

<script>
export default {
  name: "Button",

  props: {
    to: String,
    content: String,
    type: String,
    block: Boolean,
    disabled: Boolean,
    bgSky: Boolean,
    dark: Boolean,
    smallRadius: Boolean,
    roundedRadius: Boolean,
  },
};
</script>

<style scoped>
button {
  margin-top: 2rem;
  background: transparent;
}

.sky {
  background-image: linear-gradient(to left, #0096af, #0093ad80);
}

.fakelink__roundedradius {
  border-radius: 50%;
}

.fakelink__smallradius {
  border-radius: 3rem;
}

@media (min-width: 320px) and (max-width: 767px) {
  #pricing .btn {
    padding: 0.7rem 0.2rem;
  }
}
</style>