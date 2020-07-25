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
              <b-nav-item href="#">
                <font-awesome-icon :icon="['fas', 'home']" />الرئيسية
              </b-nav-item>
              <b-nav-item href="#">
                <font-awesome-icon :icon="['fas', 'eye']" />الخدمات
              </b-nav-item>
              <b-nav-item href="#">
                <font-awesome-icon :icon="['fas', 'hospital-alt']" />عن الكحّال
              </b-nav-item>
              <b-nav-item href="#">
                <font-awesome-icon :icon="['fas', 'paper-plane']" />اتصل بنا
              </b-nav-item>
            </b-navbar-nav>

            <b-navbar-nav class="action-links mr-auto">
              <b-nav-item href="#" class="action-link">
                <font-awesome-icon :icon="['fas', 'paper-plane']" />احجز موعد
              </b-nav-item>
            </b-navbar-nav>
          </b-collapse>
        </b-container>
      </b-navbar>
      <!-- <div class="bottom-svg nav-svg">
        <svg
          class="divider--hills"
          viewBox="0 0 1920 105"
          xmlns="http://www.w3.org/2000/svg"
          preserveAspectRatio="none"
          role="img"
          aria-hidden="true"
          focusable="false"
        >
          <g fill-rule="evenodd" transform="matrix(1 0 0 -1 0 105)">
            <path
              d="m1920 14.8827052c-116.23325 0-224.05162 88.3906828-395.09265 88.3906828-160.92196 0-254.53172-83.4344997-444.90735-83.4344997-154.297581 0-240.095847 39.6344097-367.66819 39.6344097-154.121863 0-198.902329-36.1223133-349.458242-36.1223133-144.878137 0-241.175717 80.8685493-362.873568 80.8685493 0-34.0793243 0-68.1494291 0-102.219534h1920z"
            />
            <path
              d="m1920 14.6612844c-116.11434 0-223.9659 88.8291396-395.06196 88.8291396-160.92415 0-254.54487-83.7874573-444.93804-83.7874573-154.317311 0-240.088941 39.8974838-367.565152 39.8974838-154.034172 0-198.792715-36.4840402-349.164477-36.4840402-144.965828 0-241.283139 81.1250467-363.270371 81.1250467 0-34.7474052 0-69.4948104 0-104.241457h1920z"
            />
          </g>
        </svg>
      </div> -->
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
  font-weight: bold;
  margin-right: 1rem;
}

.nav-link svg {
  color: #a9abad;
  margin-left: 0.5rem;
  font-size: 1.1em;
}

.action-link .nav-link {
  background-image: linear-gradient(to left, #0096af, #0093ad80);
  color: #fff !important;
  border-radius: 5rem;
  font-weight: normal !important;
}

.action-link .nav-link svg {
  color: #fff;
}
</style>