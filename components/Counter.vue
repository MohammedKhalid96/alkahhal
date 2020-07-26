<template>
  <div class="counter text-center section">
    <b-container>
      <b-row>
        <b-col cols="6" md="3">
          <div id="counter-1" class="counter__box">
            <div class="counter__box__name">
              <Title big title="عملية ناجحة" />
            </div>

            <div class="counter__box__number">
              <span
                v-countUp:onWindowScroll.once="{ watchedElId: 'counter-1', startValue: 0, endValue: 320, options: { duration: 3 } }"
              ></span>
            </div>
          </div>
        </b-col>

        <b-col cols="6" md="3">
          <div id="counter-2" class="counter__box">
            <div class="counter__box__name">
              <Title big title="فروع" />
            </div>

            <div class="counter__box__number">
              <span
                v-countUp:onWindowScroll.once="{ watchedElId: 'counter-2', startValue: 0, endValue: 2, options: { duration: 2 } }"
              ></span>
            </div>
          </div>
        </b-col>

        <b-col cols="6" md="3">
          <div id="counter-3" class="counter__box">
            <div class="counter__box__name">
              <Title big title="شركاء" />
            </div>

            <div class="counter__box__number">
              <span
                v-countUp:onWindowScroll.once="{ watchedElId: 'counter-1', startValue: 0, endValue: 25, options: { duration: 2 } }"
              ></span>
            </div>
          </div>
        </b-col>

        <b-col cols="6" md="3">
          <div id="counter-4" class="counter__box">
            <div class="counter__box__name">
              <Title big title="خدمات" />
            </div>

            <div class="counter__box__number">
              <span
                v-countUp:onWindowScroll.once="{ watchedElId: 'counter-1', startValue: 0, endValue: 15, options: { duration: 2 } }"
              ></span>
            </div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "Counter",
};
</script>

<style scoped>
.counter__box__number span {
  color: #a9abad;
  font-size: 2em;
  font-weight: bold;
}
</style>