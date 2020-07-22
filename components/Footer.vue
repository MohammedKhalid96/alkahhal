<template>
  <div class="footer">
    <b-container>
      <b-row>
        <b-col>
          <div class="footer__about">
            <div class="footer__about__logo">
              <b-img-lazy src="../assets/images/logo-white.png" fluid></b-img-lazy>
            </div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer {
}

.footer__about__logo img {
  width: 9rem;
}
</style>