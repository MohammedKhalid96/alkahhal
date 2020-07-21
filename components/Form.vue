<template>
  <div class="form">
    <b-form>
      <div class="form-select-branch-doctor text-center">
        <b-row>
          <b-col md="6">
            <div class="form-radio select-branch">
              <b-form-group>
                <b-form-radio v-model="selectedBranch" name="some-radios" value="A">فرع الدمام</b-form-radio>
                <b-form-radio v-model="selectedBranch" name="some-radios" value="B">فرع الأحساء</b-form-radio>
              </b-form-group>
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
                <b-input id="inline-form-input-name" class="mb-2 mb-sm-0" placeholder="اسم المريض"></b-input>
              </b-form-group>
            </div>
          </b-col>

          <b-col md="6">
            <div class="patient-phone">
              <b-form-group>
                <b-input id="inline-form-input-name" class="mb-2 mb-sm-0" placeholder="رقم الهاتف"></b-input>
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
        <b-button variant="primary">إرسال</b-button>
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
}

.form-inline .form-control {
  width: 100%;
}

.form-radio .custom-control {
  display: inline-block;
  margin-left: 1rem;
}
</style>