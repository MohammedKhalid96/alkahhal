<template>
  <b-button
    class="button__element"
    :to="to"
    :block="block"
    :disabled="disabled"
    :type="type"
    :size="size"
    :class="{fakelink__roundedradius: roundedRadius, fakelink__smallradius: smallRadius, transparent: transparent, sky: bgSky, border: border}"
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
    size: String,
    block: Boolean,
    disabled: Boolean,
    bgSky: Boolean,
    transparent: Boolean,
    border: Boolean,
    smallRadius: Boolean,
    roundedRadius: Boolean,
  },
};
</script>

<style scoped>
button {
  background: transparent;
  color: #fff;
}

.sky {
  background: #11799a;
  font-weight: bold;
}

.transparent {
  background: transparent;
  border: 1px solid #11799a;
  color: #11799a;
}

.fakelink__roundedradius {
  border-radius: 50%;
}

.fakelink__smallradius {
  border-radius: 3rem;
}

.border {
  border: 3px solid #f2c916 !important;
}

@media (min-width: 320px) and (max-width: 767px) {
}
</style>