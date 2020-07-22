<template>
  <div class="contact section">
    <b-container>
      <b-row>
        <b-col md="6">
          <div class="contact-info flex-center">
            <ul>
              <li>
                <a :href="'tel:'+contactInfoHotLine">
                  <font-awesome-icon :icon="['fas', 'mobile-alt']" />
                  <span class="contact-info__name">الخط الساخن</span>
                  {{contactInfoHotLine}}
                </a>
              </li>
              <li>
                <a :href="'mailto:'+contactInfoEmail">
                  <font-awesome-icon :icon="['fas', 'envelope']" />
                  <span class="contact-info__name">البريد الألكتروني</span>
                  {{contactInfoEmail}}
                </a>
              </li>
              <li>
                <a
                  target="_blank"
                  href="https://www.google.com.eg/maps/place/%D9%85%D8%AC%D9%85%D8%B9+%D8%A7%D9%84%D9%83%D8%AD%D8%A7%D9%84+%D8%A7%D9%84%D8%B7%D8%A8%D9%8A%E2%80%AD/@26.4737274,50.0957093,18z/data=!3m1!4b1!4m5!3m4!1s0x3e49fea90b63e9b5:0xa6d890753e9d119!8m2!3d26.4737274!4d50.094615"
                >
                  <font-awesome-icon :icon="['fas', 'map']" />
                  <span class="contact-info__name">فرع الدمام</span>
                  {{contactInfoAddressDammam}}
                </a>
              </li>

              <li>
                <a
                  target="_blank"
                  href="https://www.google.com.eg/maps/place/%D8%AA%D9%83%D9%86%D9%88+%D8%B9%D8%A7%D9%84%D9%85+%D8%A7%D9%84%D8%A5%D9%84%D9%83%D8%AA%D8%B1%D9%88%D9%86%D9%8A%D8%A7%D8%AA%E2%80%AD/@25.4344079,49.5729103,20.08z/data=!4m12!1m6!3m5!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!2z2KrZg9mG2Ygg2LnYp9mE2YUg2KfZhNil2YTZg9iq2LHZiNmG2YrYp9iq!8m2!3d25.4344162!4d49.5725679!3m4!1s0x3e37bd80e83b39fd:0x5b449c0991e17513!8m2!3d25.4344162!4d49.5725679"
                >
                  <font-awesome-icon :icon="['fas', 'map']" />
                  <span class="contact-info__name">فرع الأحساء</span>
                  {{contactInfoAddressAlhesa}}
                </a>
              </li>
            </ul>
          </div>
        </b-col>

        <b-col md="6">
          <div class="contact-form">
            <Form />
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Title from "./Title";
import Form from "./Form";

export default {
  name: "Contact",

  components: { Title, Form },

  data() {
    return {
      contactInfoHotLine: "0553809777",
      contactInfoEmail: "alkahhalmedicalcomplex@gmail.com",
      contactInfoAddressDammam:
        "7672 ابو قيس الجهني, حي الحمراء, الدمام, السعودية",
      contactInfoAddressAlhesa: "الأحساء, محاسن, المبرز"
    };
  }
};
</script>

<style scoped>
.contact-info li {
  margin-bottom: 2rem;
}

.contact-info a {
  color: #0096af;
  font-size: 1.1em;
}

.contact-info svg {
  margin-left: 0.5rem;
}

.contact-info .contact-info__name {
  color: #a9abad;
}
</style>