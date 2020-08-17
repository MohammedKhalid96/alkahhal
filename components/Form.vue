<template>
  <div class="form relative">
    <b-form>
      <div class="form-patient-info">
        <b-row>
          <b-col md="6">
            <div class="form-radio patient-name">
              <b-form-group>
                <b-input
                  name="name"
                  id="inline-form-input-name"
                  class="mb-2"
                  placeholder="الاسم بالكامل"
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
                  placeholder="رقم الجوال"
                  required
                ></b-input>
              </b-form-group>
            </div>
          </b-col>
        </b-row>
      </div>

      <div class="form-select-branch-doctor mb-4 text-center">
        <div class="form-radio select-branch">
          <b-form-radio-group name="branch" buttons :value="selectedBranch" required>
            <b-form-radio v-model="selectedBranch" value="Dmamm branch" required>
              <font-awesome-icon :icon="['fas', 'circle']" />فرع الدمام
            </b-form-radio>
            <b-form-radio v-model="selectedBranch" value="Ahsa branch" required>
              <font-awesome-icon :icon="['fas', 'circle']" />فرع الأحساء
            </b-form-radio>
          </b-form-radio-group>
        </div>
      </div>

      <div class="form-submit-btn text-center">
        <b-button type="submit" class="action-btn">
          <font-awesome-icon :icon="['fas', 'calendar-check']" />احجز الآن
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
      selectedBranch: "",
    };
  },
};
</script>

<style scoped>
.form {
  border-radius: 5rem;
  color: #11799a;
  font-weight: bold;
}

.form-inline .form-control {
  width: 100%;
}

.form-radio .custom-control {
  display: inline-block;
  margin-left: 1rem;
}

.select-branch .btn {
  background: transparent;
  border: 1px solid #fff !important;
  color: #fff;
  border-radius: 5rem !important;
  padding: 0.6rem 1.6rem;
  padding-top: 0.3rem;
  margin-left: 0.3rem;
  font-weight: bold;
}

.select-branch .btn.active {
  background: #fff;
  border: 0;
  -webkit-box-shadow: none;
  box-shadow: none;
  color: #11799a;
}

.select-doctor {
  cursor: pointer;
}

@media (min-width: 992px) and (max-width: 1183px) {
}

@media (min-width: 768px) and (max-width: 991px),
  screen and (min-width: 320px) and (max-width: 767px) {
  .form {
    padding: 0;
  }



  .select-branch {
    text-align: center;
    margin-bottom: 2rem;
  }

  .form::before {
    top: -3vh;
  }

  .select-branch .btn {
    padding: 0.3rem 0.8rem 0.6rem 0.8rem !important;
  }
}
</style>