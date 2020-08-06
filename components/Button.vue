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
  margin-top: 3rem;
  background: transparent;
  color: #fff;
}

.sky {
  background: #f2c916;
  font-weight: bold;
}

.fakelink__roundedradius {
  border-radius: 50%;
}

.fakelink__smallradius {
  border-radius: 3rem;
}

@media (min-width: 320px) and (max-width: 767px) {
}
</style>