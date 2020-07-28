<template>
  <header>
    <div class="navbar relative">
      <b-navbar toggleable="lg" type="dark" variant="info">
        <b-container>
          <b-navbar-brand href="#" class="ml-auto">
            <b-img src="../assets/images/logo.png" fluid alt="alkahhal logo"></b-img>
          </b-navbar-brand>

          <b-navbar-nav class="m-auto">
            <b-nav-item href="tel:0553809777">
              <b-img src="../assets/images/icons/phone.svg"></b-img>0553809777
            </b-nav-item>
          </b-navbar-nav>

          <b-navbar-nav class="mr-auto">
            <b-nav-item href="#" v-scroll-to="'#contact'" class="action-link">
              <font-awesome-icon :icon="['fas', 'paper-plane']" />احجز موعد
            </b-nav-item>
          </b-navbar-nav>
        </b-container>
      </b-navbar>
    </div>
  </header>
</template>

<script>
export default {
  name: "Nav2",
};
</script>

<style scoped>
header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
}

.navbar {
  width: 100%;
  padding: 0.5rem 0 0.5rem 0;
  margin: 0;
  -webkit-box-align: inherit;
  -ms-flex-align: inherit;
  align-items: inherit;
}

.bg-info {
  background: transparent !important;
  background-size: cover !important;
}

.navbar-brand img {
  width: 9rem;
}

.navbar-brand {
  margin-right: 0;
}

.navbar-dark .navbar-nav .nav-link {
  padding: 0.5rem 1rem 0.8rem 1rem !important;
  font-size: 1.1em;
  color: #0096af;
  font-weight: bold;
}

.nav-link img {
  margin-left: 0.5rem;
  width: 2rem;
}

.nav-link svg {
  margin-left: 0.5rem;
}

.action-link .nav-link {
  background-image: -webkit-gradient(
    linear,
    right top,
    left top,
    from(#0096af),
    to(#0093ad80)
  );
  background-image: -o-linear-gradient(right, #0096af, #0093ad80);
  background-image: linear-gradient(to left, #0096af, #0093ad80);
  color: #fff !important;
  border-radius: 5rem;
  font-weight: normal !important;
}

.action-link {
  margin-bottom: 0.3rem;
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 321px) and (max-width: 767px) {
  .navbar-brand img {
    width: 5.5rem;
  }

  .navbar-nav {
    margin-right: 0;
  }

  .navbar-dark .navbar-nav .nav-link {
    font-size: 0.9em;
    margin-right: 0;
    padding: 0.3rem 0.8rem 0.6rem 0.8rem !important;
  }
}

@media (max-width: 320px) {
  .navbar-brand img {
    width: 4rem;
  }

  .navbar-dark .navbar-nav .nav-link {
    font-size: 0.7em;
    padding: 0.3rem 0.5rem 0.6rem 0.5rem !important;
  }
}
</style>