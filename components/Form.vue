<template>
  <div class="form">
    <b-form>
      <div class="form-select-branch-doctor mb-2">
        <b-row>
          <b-col md="6">
            <div class="form-radio select-branch">
              <b-form-radio-group buttons button-variant="outline-primary">
                <b-form-radio v-model="selectedBranch" name="some-radios" value="A">فرع الدمام</b-form-radio>
                <b-form-radio v-model="selectedBranch" name="some-radios" value="B">فرع الأحساء</b-form-radio>
              </b-form-radio-group>
            </div>
          </b-col>

          <b-col md="6">
            <div class="form-dropdown select-doctor">
              <b-form-group>
                <b-form-select v-model="selectedDoctor" :options="options"></b-form-select>
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
                <b-input id="inline-form-input-name" class="mb-2" placeholder="اسم المريض"></b-input>
              </b-form-group>
            </div>
          </b-col>

          <b-col md="6">
            <div class="patient-phone">
              <b-form-group>
                <b-input id="inline-form-input-name" class="mb-2" placeholder="رقم الهاتف"></b-input>
              </b-form-group>
            </div>
          </b-col>
        </b-row>
      </div>

      <div class="form-date-time">
        <b-row>
          <b-col md="6">
            <div class="select-date">
              <b-form-group>
                <b-form-datepicker
                  id="example-datepicker"
                  v-model="dateValue"
                  class="mb-2"
                  locale="ar"
                ></b-form-datepicker>
              </b-form-group>
            </div>
          </b-col>

          <b-col md="6">
            <div class="select-time">
              <b-form-timepicker v-model="timeValue" locale="ar"></b-form-timepicker>
            </div>
          </b-col>
        </b-row>
      </div>

      <div class="form-submit-btn text-center">
        <b-button class="action-btn">إرسال</b-button>
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
        { value: "د. عادل عبدالعزيز الرشود", text: "د. عادل عبدالعزيز الرشود" }
      ]
    };
  }
};
</script>

<style scoped>
.form {
  padding: 4rem;
  background: #fff;
  background-size: contain;
  border-radius: 5rem;
  color: #0096af;
  font-weight: bold;
}

.form-inline .form-control {
  width: 100%;
}

.form-radio .custom-control {
  display: inline-block;
  margin-left: 1rem;
}

.select-branch .btn-outline-primary {
  border: 1px solid #0096af !important;
  color: #0096af;
  border-radius: 5rem !important;
  padding: 0.6rem 1.6rem;
  padding-top: 0.3rem;
  margin-left: 0.3rem;
}

.select-branch .btn-outline-primary:not(:disabled):not(.disabled):active,
.btn-outline-primary:not(:disabled):not(.disabled).active,
.show > .btn-outline-primary.dropdown-toggle {
  background: transparent;
  background-image: linear-gradient(to left, #0096af, rgba(0, 147, 173, 0.5));
  border: 0;
  box-shadow: none;
  color: #fff;
}
</style>