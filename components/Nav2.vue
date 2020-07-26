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
  margin-right: 1rem;
}

.nav-link img {
  margin-left: 0.5rem;
  width: 2rem;
}

.nav-link svg {
  margin-left: 0.5rem;
}

.action-link .nav-link {
  background-image: linear-gradient(to left, #0096af, #0093ad80);
  color: #fff !important;
  border-radius: 5rem;
  font-weight: normal !important;
}

@media (min-width: 992px) and (max-width: 1183px) {
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 320px) and (max-width: 767px) {
  .top-navbar {
    display: none;
  }

  .navbar-brand img {
    width: 7rem;
  }

  .navbar-nav {
    margin-right: 0;
    margin-top: 1rem;
  }

  .navbar-dark .navbar-nav .nav-link {
    margin-bottom: 1rem;
    margin-right: 0;
  }

  .action-link .nav-link {
    text-align: center;
  }
}
</style>