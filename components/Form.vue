<template>
  <div class="form relative">
    <b-form>
      <div class="form-select-branch-doctor mb-2">
        <b-row>
          <b-col md="6">
            <div class="form-radio select-branch">
              <b-form-radio-group name="branch" buttons :value="selectedBranch">
                <b-form-radio v-model="selectedBranch" value="Dmamm branch" required>فرع الدمام</b-form-radio>
                <b-form-radio v-model="selectedBranch" value="Ahsa branch" required>فرع الأحساء</b-form-radio>
              </b-form-radio-group>
            </div>
          </b-col>

          <b-col md="6">
            <div class="form-dropdown select-doctor">
              <b-form-group>
                <b-form-select name="doctor" v-model="selectedDoctor" :options="options" required></b-form-select>
              </b-form-group>
            </div>
          </b-col>
        </b-row>
      </div>

      <div class="form-patient-info">
        <b-row>
          <b-col md="6">
            <div class="form-radio patient-name">
              <b-form-group>
                <b-input
                  name="name"
                  id="inline-form-input-name"
                  class="mb-2"
                  placeholder="اسم المريض"
                  required
                ></b-input>
              </b-form-group>
            </div>
          </b-col>

          <b-col md="6">
            <div class="patient-phone">
              <b-form-group>
                <b-input
                  name="phone"
                  id="inline-form-input-name"
                  class="mb-2"
                  placeholder="رقم الهاتف"
                  required
                ></b-input>
              </b-form-group>
            </div>
          </b-col>
        </b-row>
      </div>

      <div class="form-date-time">
        <b-row>
          <b-col md="6">
            <div class="select-date">
              <b-form-group name="datepicker" :value="dateValue">
                <b-form-datepicker
                  id="example-datepicker"
                  v-model="dateValue"
                  class="mb-2dsdsdsdsd"
                  locale="ar"
                ></b-form-datepicker>
              </b-form-group>
            </div>
          </b-col>

          <b-col md="6">
            <div class="select-time">
              <b-form-group name="timepicker" :value="timeValue">
                <b-form-timepicker v-model="timeValue" locale="ar"></b-form-timepicker>
              </b-form-group>
            </div>
          </b-col>
        </b-row>
      </div>

      <div class="form-submit-btn text-center">
        <b-button type="submit" class="action-btn">
          <font-awesome-icon :icon="['fas', 'paper-plane']" />إرسال
        </b-button>
      </div>
    </b-form>
  </div>
</template>

<script>
export default {
  name: "Form",

  data() {
    return {
      dateValue: "",
      timeValue: "",
      selectedBranch: "",
      selectedDoctor: null,
      options: [
        { value: null, text: "اسم الطبيب" },
        { value: "د. إلهام التميمي", text: "د. إلهام التميمي" },
        { value: "د. عادل عبدالعزيز الرشود", text: "د. عادل عبدالعزيز الرشود" },
      ],
    };
  },
};
</script>

<style scoped>
.form {
  padding: 4rem;
  background: #fff;
  background-size: cover;
  border-radius: 5rem;
  color: #0096af;
  font-weight: bold;
}

.form::before {
  position: absolute;
  width: 100%;
  content: "";
  z-index: -2;
  top: -6vh;
  right: -6vh;
  bottom: -4vh;
  max-width: 69.7%;
  opacity: 1;
  background-image: radial-gradient(#0096af 6%, transparent 0);
  background-size: 35px 35px;
}

#example-datepicker__outer_ {
  direction: ltr;
}

.form-inline .form-control {
  width: 100%;
}

.form-radio .custom-control {
  display: inline-block;
  margin-left: 1rem;
}

.select-branch .btn {
  background: #fff;
  border: 1px solid #0096af !important;
  color: #0096af;
  border-radius: 5rem !important;
  padding: 0.6rem 1.6rem;
  padding-top: 0.3rem;
  margin-left: 0.3rem;
}

.select-branch .btn.active {
  background: transparent;
  background: linear-gradient(to left, #0096af, rgba(0, 147, 173, 0.5));
  border: 0;
  box-shadow: none;
  color: #fff;
}

.select-doctor {
  cursor: pointer;
}

@media (min-width: 992px) and (max-width: 1183px) {
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 320px) and (max-width: 767px) {
  .form {
    padding: 2rem 1rem;
  }

  .select-branch {
    text-align: center;
    margin-bottom: 2rem;
  }
}
</style>