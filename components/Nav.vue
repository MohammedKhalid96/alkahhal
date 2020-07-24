<template>
  <header>
    <div class="top-navbar">
      <b-container>
        <b-row>
          <b-col md="8">
            <div class="top-navbar__right">
              <a
                target="_blank"
                href="https://www.google.com.eg/maps/place/%D9%85%D8%AC%D9%85%D8%B9+%D8%A7%D9%84%D9%83%D8%AD%D8%A7%D9%84+%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%E2%80%AD/@26.4737274,50.0957093,18z/data=!3m1!4b1!4m5!3m4!1s0x3e49fea90b63e9b5:0xa6d890753e9d119!8m2!3d26.4737274!4d50.094615"
              >
                <b-img src="../assets/images/icons/location-white.svg" fluid></b-img>
                <span class="contact-info__name">فرع الدمام</span>
                7672 ابو قيس الجهني, حي الحمراء, الدمام, السعودية
              </a>

              <a
                target="_blank"
                href="https://www.google.com.eg/maps/place/%D9%85%D8%AC%D9%85%D8%B9+%D8%A7%D9%84%D9%83%D8%AD%D8%A7%D9%84+%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%E2%80%AD/@26.4737274,50.0957093,18z/data=!3m1!4b1!4m5!3m4!1s0x3e49fea90b63e9b5:0xa6d890753e9d119!8m2!3d26.4737274!4d50.094615"
              >
                <b-img src="../assets/images/icons/location-white.svg" fluid></b-img>
                <span class="contact-info__name">فرع الدمام</span>
                الأحساء, محاسن, المبرز
              </a>
            </div>
          </b-col>

          <b-col md="4">
            <div class="top-navbar__left text-left">
              <a href target="_blank" rel="noopener noreferrer">
                <b-img src="../assets/images/icons/phone-white.svg" fluid></b-img>
              </a>
              <a href target="_blank" rel="noopener noreferrer">
                <font-awesome-icon :icon="['fab', 'facebook']" />
              </a>

              <a href target="_blank" rel="noopener noreferrer">
                <font-awesome-icon :icon="['fab', 'twitter']" />
              </a>

              <a href target="_blank" rel="noopener noreferrer" class="ml-0">
                <font-awesome-icon :icon="['fab', 'instagram']" />
              </a>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </div>
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
              <b-nav-item href="#" class="action-link">احجز موعد</b-nav-item>
            </b-navbar-nav>
          </b-collapse>
        </b-container>
      </b-navbar>
      <!-- <div class="bottom-shape">
      <b-img src="../assets/images/bg-bottom.png" fluid-grow></b-img>
      </div>-->
    </div>
  </header>
</template>

<script>
export default {
  name: "Nav",
};
</script>

<style scoped>
.top-navbar {
  background-image: linear-gradient(to left, #0096af, rgba(0, 147, 173, 0.6));
  padding: 0.5rem 0;
}

.top-navbar a {
  color: #fff;
  margin-left: 1rem;
}

.top-navbar svg {
  margin-left: 0.5rem;
}

.top-navbar img {
  width: 20px;
}

.navbar {
  width: 100%;
  padding: 0.5rem 0 0.5rem 0;
  margin: 0;
  align-items: inherit;
}

.bg-info {
  /* background: linear-gradient(to left bottom, #fff 40%, #ffffff59, transparent),
    url("../assets/images/pattern-2.png") !important; */
  background: #fff !important;
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
  font-size: 1.1em;
  color: #0096af;
}

.action-link .nav-link {
  background-image: linear-gradient(to left, #0096af, #0093ad80);
  color: #fff !important;
  border-radius: 5rem;
}
</style>