<template>
  <header>
    <div class="navbar relative">
      <b-navbar toggleable="lg" type="dark" variant="info" fixed="top">
        <b-container>
          <b-navbar-brand to="/" class="ml-auto">
            <b-img src="../assets/images/logo.png" fluid alt="alkahhal logo"></b-img>
          </b-navbar-brand>

          <b-navbar-nav class="mr-auto">
            <b-nav-item to="/" v-scroll-to="'#contact-form'" class="action-link">
              <span class="btn-anim"></span>
              <font-awesome-icon :icon="['fas', 'calendar-check']" />احجز الآن
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
  background: transparent;
}

.navbar {
  width: 90%;
  padding: 0.5rem 0 0.5rem 0;
  margin: 0;
  -webkit-box-align: inherit;
  -ms-flex-align: inherit;
  align-items: inherit;
}

.fixed-top {
  right: auto;
  left: 50% !important;
  -webkit-transform: translateX(-50%);
  -ms-transform: translateX(-50%);
  transform: translateX(-50%);
}

.bg-info {
  background: #fff !important;
}

.navbar-brand img {
  width: 8rem;
}

.navbar-brand {
  margin-right: 0;
}

.navbar-dark .navbar-nav .nav-link {
  padding: 0.3rem 1.2rem 0.6rem 1.2rem !important;
  font-size: 1em;
  color: #5c5d5e;
}

.nav-link img {
  margin-left: 0.5rem;
  width: 2rem;
}

.nav-link svg {
  margin-left: 0.5rem;
}

.action-link .nav-link {
  background: #fff;
  color: #5c5d5e !important;
  border: 1px solid #11799a;
  border-radius: 5rem;
  -webkit-animation: offer_animation 2s infinite;
  -moz-animation: offer_animation 2s infinite;
  -o-animation: offer_animation 2s infinite;
  animation: offer_animation 2s infinite;
}

.action-link .nav-link svg {
  color: #11799a;
}

.action-link {
  position: relative;
  margin-bottom: 0.4rem;
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 321px) and (max-width: 767px) {
  .navbar {
    width: 100%;
    padding: 0.5rem 0.3rem;
  }
  
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
  .navbar {
    width: 100%;
    padding: 0.5rem 0.3rem;
  }

  .navbar-brand img {
    width: 4rem;
  }

  .navbar-dark .navbar-nav .nav-link {
    font-size: 0.7em;
    padding: 0.3rem 0.5rem 0.6rem 0.5rem !important;
  }
}
</style>