<template>
  <div class="container">
    <!-- 1st row -->
    <h3>my Father info</h3>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Father Name"
          :value="studentInfo.fatherName"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Father Name"
          v-model="studentInfo.fatherName"
          v-if="editable === true"
          v-validate="{ alpha_spaces: true }"
          name="fathername"
        >
        <div class="err">{{ errors.first('fathername') }}</div>
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Father Occupation"
          :value="studentInfo.fatherOccupation"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Father Occupation"
          v-model="studentInfo.fatherOccupation"
          v-if="editable === true"
        >
      </div>

    </div>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Father Mobile Number"
          :value="studentInfo.fatherMobileNumber"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Father Mobile Number"
          v-model="studentInfo.fatherMobileNumber"
          v-if="editable === true"
          v-validate="{ numeric: true, required: false }"
          name="father mobile number"
        >
        <div class="err">{{ errors.first('father mobile number') }}</div>
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Father Landline Number"
          :value="studentInfo.fatherLandlineNumber"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Father Landline Number"
          v-model="studentInfo.fatherLandlineNumber"
          v-if="editable === true"
          v-validate="{ numeric: true, required: false }"
          name="father landline number"
        >
        <div class="err">{{ errors.first('father landline number') }}</div>
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Father Religion"
          :value="studentInfo.fatherReligion"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Father Religion"
          v-model="studentInfo.fatherReligion"
          v-if="editable === true"
        >
      </div>
    </div>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Father Educational Attainment"
          :value="studentInfo.fatherEducation"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Father Educational Attainment"
          v-model="studentInfo.fatherEducation"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Father School Graduated"
          :value="studentInfo.fatherSchool"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Father School Graduated"
          v-model="studentInfo.fatherSchool"
          v-if="editable === true"
        >
      </div>
    </div>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Father Employer"
          :value="studentInfo.fatherEmployer"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Father Employer"
          v-model="studentInfo.fatherEmployer"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Father Employer Address"
          :value="studentInfo.fatherEmpolyerAddress"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Father Employer Address"
          v-model="studentInfo.fatherEmployerAddress"
          v-if="editable === true"
        >
      </div>
    </div>

    <h3>my Mother info</h3>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Mother Name with Maiden Name"
          :value="studentInfo.motherName"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Mother Name with Maiden Name"
          v-model="studentInfo.motherName"
          v-if="editable === true"
          v-validate="{ alpha_spaces: true }"
          name="mother name"
        >
        <div class="err">{{ errors.first('mother name') }}</div>
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Mother Occupation"
          :value="studentInfo.motherOccupation"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Mother Occupation"
          v-model="studentInfo.motherOccupation"
          v-if="editable === true"
        >
      </div>

    </div>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Mother Mobile Number"
          :value="studentInfo.motherMobileNumber"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Mother Mobile Number"
          v-model="studentInfo.motherMobileNumber"
          v-if="editable === true"
          v-validate="{ numeric: true }"
          name="mobile number"
        >
        <div class="err">{{ errors.first('mother mobile name') }}</div>
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Mother Landline Number"
          :value="studentInfo.motherLandlineNumber"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Mother Landline Number"
          v-model="studentInfo.motherLandlineNumber"
          v-if="editable === true"
          v-validate="{ numeric: true }"
          name="landline number"
        >
        <div class="err">{{ errors.first('mother landline name') }}</div>
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Mother Religion"
          :value="studentInfo.motherReligion"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Mother Religion"
          v-model="studentInfo.motherReligion"
          v-if="editable === true"
        >
      </div>
    </div>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Mother Educational Attainment"
          :value="studentInfo.motherEducation"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Mother Educational Attainment"
          v-model="studentInfo.motherEducation"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Mother School Graduated"
          :value="studentInfo.motherSchool"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Mother School Graduated"
          v-model="studentInfo.motherSchool"
          v-if="editable === true"
        >
      </div>
    </div>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Mother Employer"
          :value="studentInfo.motherEmployer"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Mother Employer"
          v-model="studentInfo.motherEmployer"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Mother Employer Address"
          :value="studentInfo.motherEmployerAddress"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Mother Employer Address"
          v-model="studentInfo.motherEmployerAddress"
          v-if="editable === true"
        >
      </div>
    </div>

    <h3>Guardian</h3>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Name of Guardian"
          :value="studentInfo.guardianName"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Name of Guardian"
          v-model="studentInfo.guardianName"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Relationship to Guardian"
          :value="studentInfo.relationship"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Relationship to Guardian"
          v-model="studentInfo.relationship"
          v-if="editable === true"
        >
      </div>
    </div>

    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Guardian Mobile Number"
          :value="studentInfo.guardianMobileNumber"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Guardian Mobile Number"
          v-model="studentInfo.guardianMobileNumber"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Guardian Landline Number"
          :value="studentInfo.guardianLandlineNumber"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Guardian Landline Number"
          v-model="studentInfo.guardianLandlineNumber"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Guardian Religion"
          :value="studentInfo.guardianReligion"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Guardian Religion"
          v-model="studentInfo.guardianReligion"
          v-if="editable === true"
        >
      </div>
    </div>

    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="guardian Educational Attainment"
          :value="studentInfo.guardianEducationalAttainment"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="guardian Educational Attainment"
          v-model="studentInfo.guardianEducationalAttainment"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="guardian School Graduated"
          :value="studentInfo.guardianSchoolGraduated"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="guardian School Graduated"
          v-model="studentInfo.guardianSchoolGraduated"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="Guardian Occupation"
          :value="studentInfo.guardianOccupation"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="Guardian Occupation"
          v-model="studentInfo.guardianOccupation"
          v-if="editable === true"
        >
      </div>
    </div>
    <div class="row p-2">
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="guardian Employer"
          :value="studentInfo.guardianEmployer"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="guardian Employer"
          v-model="studentInfo.guardianEmployer"
          v-if="editable === true"
        >
      </div>
      <div class="col">
        <input
          readonly
          type="text"
          class="form-control"
          placeholder="guardian Employer Address"
          :value="studentInfo.guardianEmployerAddress"
          v-if="editable === false"
        >
        <input
          type="text"
          class="form-control"
          placeholder="guardian Employer Address"
          v-model="studentInfo.guardianEmployerAddress"
          v-if="editable === true"
        >
      </div>
    </div>
    <!-- end of container -->
  </div>
</template>

<script>
export default {
  name: "ParentInformation",
  inject: ["$validator"],
  props: ["editable", "studentInfo"]
};
</script>

<style scoped>
.err {
  color: #ff0000;
}
</style>
