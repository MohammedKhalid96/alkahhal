<template>
  <div class="navbar relative">
    <b-navbar toggleable="lg" type="dark" variant="info">
      <b-container>
        <b-navbar-brand href="#">
          <b-img src="../assets/images/logo.png" fluid alt="alkahhal logo"></b-img>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item href="#">الرئيسية</b-nav-item>
            <b-nav-item href="#">الخدمات</b-nav-item>
            <b-nav-item href="#">عن الكحّال</b-nav-item>
            <b-nav-item href="#">اتصل بنا</b-nav-item>
          </b-navbar-nav>

          <b-navbar-nav class="action-links mr-auto">
            <b-nav-item target="_blank" href="#">
              <font-awesome-icon :icon="['fab', 'facebook']" />
            </b-nav-item>
            <b-nav-item target="_blank" href="#">
              <font-awesome-icon :icon="['fab', 'instagram']" />
            </b-nav-item>
            <b-nav-item target="_blank" href="#">
              <font-awesome-icon :icon="['fab', 'twitter']" />
            </b-nav-item>
            <b-nav-item href="#" class="action-link">احجز موعد</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
    <!-- <div class="bottom-shape">
      <b-img src="../assets/images/bg-bottom.png" fluid-grow></b-img>
    </div>-->
    <div class="divider"></div>
  </div>
</template>

<script>
export default {
  name: "Nav"
};
</script>

<style scoped>
.navbar {
  width: 100%;
  padding: 0 0 0 0;
}

.bg-info {
  /* background: linear-gradient(to left bottom, #fff 40%, #ffffff59, transparent),
    url("../assets/images/pattern-2.png") !important; */
    background: transparent !important;
  background-size: cover !important;
}

.navbar-brand img {
  width: 9rem;
}

.navbar-brand {
  margin-right: 0;
}

.navbar-nav {
  margin-right: 1rem;
}

.navbar-dark .navbar-nav .nav-link {
  padding: 0.5rem 1rem 0.8rem 1rem !important;
  font-size: 1.2em;
  font-weight: bold;
  color: #0096af;
}

.action-link .nav-link {
  background-image: linear-gradient(to left, #0096af, #0093ad80);
  color: #fff !important;
  border-radius: 5rem;
}
</style>