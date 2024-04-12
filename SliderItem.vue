<template>
  <div class="row" style="background-color: white !important">
    <div class="col-1"></div>
    <div class="col-lg-3 col-md-3 col-sm-12 col-xs-12">
      <q-item class="logo-padding">
        <q-img
          class="absolute-middle"
          src="../assets/Hyperhire.png"
          style="width: 35%; height: 35%"
        >
        </q-img>
      </q-item>
      <q-item>
        <p class="sub_header1">Do developers need it?</p>
      </q-item>
      <q-item class="description_content">
        Average monthly salary of 120 million won is calculated based on the
        relevant country.
      </q-item>
      <q-item class="description_content">010-0000-0000</q-item>
      <q-item class="description_content">aaaaa@naver.com</q-item>
      <q-item class="description_content"
        >Hyperhire India Private Limited</q-item
      >
      <q-item class="description_content">ⓒ 2023 Hyperhire</q-item>
    </div>
    <div class="col-8 col-md-8 col-sm-12 col-xs-12 q-mt-lg">
      <div class="row">
        <div class="col-3">
          <q-chip icon="event"></q-chip>
          <q-item class="description_content">해외 개발자 원격 채용</q-item>
        </div>
        <div class="col-3">
          <q-chip icon="alarm"></q-chip>
          <q-item class="description_content">외국인 원격 채용 (비개발)</q-item>
        </div>
        <div class="col-3">
          <q-chip icon="bookmark"></q-chip>
          <q-item class="description_content">한국어 가능 외국인 채용</q-item>
        </div>
        <div class="col-3">
          <q-chip icon="directions"></q-chip>
          <q-item class="description_content">해외 개발자 활용 서비스</q-item>
        </div>
      </div>
      <q-space />
      <div class="row">
        <div class="col-3 col-md-3 col-sm-12 col-xs-12 q-mt-lg">
          <q-space></q-space>
          <q-item class="description_content">사업자등록번호 CIN</q-item>
          <q-item class="description_content">427-86-01187</q-item>
          <q-item class="description_content">U74110DL2016PTC290812</q-item>
        </div>
        <div class="col-6 col-md-6 col-sm-12 col-xs-12 q-mt-lg">
          <q-space></q-space>
          <q-item class="description_content">ADDRESS</q-item>
          <q-item class="description_content"
            >D-138, Street number 11, Jagjeet Nagar, North East Delhi, New
            Delhi, 110053 India</q-item
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.logo-padding {
  padding: 6px 0px 6px 16px !important;
}
.sub_header1 {
  text-transform: capitalize !important;
  font-weight: 400 !important;
  color: rgb(39, 38, 38) !important;
  letter-spacing: 0.2px !important;
  margin: 0px !important;
  font-size: 1.05em !important;
}
.description_content {
  color: rgb(49, 48, 48) !important;
  line-height: 18px !important;
  padding: 4px 16px !important;
  min-height: 0px !important;
  font-weight: 600 !important;
}
</style>
