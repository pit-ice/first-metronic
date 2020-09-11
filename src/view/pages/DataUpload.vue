<template>
  <div class="card card-custom">
    <!--begin::Header-->
    <div class="card-header border-0 pt-5">
      <h2 class="card-title font-weight-bolder">
        데이터 세트 등록하기
      </h2>
    </div>
    <!--end::Header-->
    <div class="card-body p-0">
      <!--begin: Wizard-->
      <div
        class="wizard wizard-2"
        id="kt_wizard_v2"
        data-wizard-state="step-first"
        data-wizard-clickable="true"
      >
        <!--begin: Wizard Nav -->
        <div class="wizard-nav border-right py-8 px-8 py-lg-20 px-lg-10">
          <div class="wizard-steps">
            <div
              class="wizard-step"
              data-wizard-type="step"
              data-wizard-state="current"
            >
              <div class="wizard-wrapper">
                <div class="wizard-icon">
                  <span class="svg-icon svg-icon-2x">
                    <inline-svg src="/media/svg/icons/General/Edit.svg" />
                  </span>
                </div>
                <div class="wizard-label">
                  <h3 class="wizard-title">
                    1. 기본정보 입력하기
                  </h3>
                  <div class="wizard-desc">
                    데이터 세트의 기본 정보 입력
                  </div>
                </div>
              </div>
            </div>
            <div class="wizard-step" data-wizard-type="step">
              <div class="wizard-wrapper">
                <div class="wizard-icon">
                  <span class="svg-icon svg-icon-2x">
                    <inline-svg src="/media/svg/icons/Files/Upload.svg" />
                  </span>
                </div>
                <div class="wizard-label">
                  <h3 class="wizard-title">
                    2. 데이터 파일 업로드
                  </h3>
                  <div class="wizard-desc">
                    등록할 데이터 파일 업로드
                  </div>
                </div>
              </div>
            </div>
            <div class="wizard-step" href="#" data-wizard-type="step">
              <div class="wizard-wrapper">
                <div class="wizard-icon">
                  <span class="svg-icon svg-icon-2x">
                    <inline-svg src="/media/svg/icons/Text/Toggle-Right.svg" />
                  </span>
                </div>
                <div class="wizard-label">
                  <h3 class="wizard-title">
                    3. 세부정보 확인
                  </h3>
                  <div class="wizard-desc">
                    세부정보 확인 후 데이터 등록 완료
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!--end: Wizard Nav -->

        <!--begin: Wizard Body -->
        <div class="wizard-body py-8 px-8 py-lg-20 px-lg-10">
          <!--begin: Wizard Form-->
          <div class="row">
            <div class="offset-xxl-2 col-xxl-8">
              <form class="form" id="kt_form">
                <!--begin: Wizard Step 1-->
                <div
                  class="pb-5"
                  data-wizard-type="step-content"
                  data-wizard-state="current"
                >
                  <h4 class="mb-10 font-weight-bold text-dark">
                    기본 정보 입력
                  </h4>
                  <div class="form-group">
                    <label>데이터셋 이름 *</label>
                    <input
                      type="text"
                      class="form-control form-control-solid form-control-lg"
                      name="fname"
                      placeholder="데이터셋 이름"
                    />
                    <span class="form-text text-muted"
                      >Please enter dataset name.</span
                    >
                  </div>
                  <div class="form-group">
                    <label>데이터셋 설명</label>
                    <textarea
                      type="text"
                      class="form-control form-control-solid form-control-lg"
                      name="fname"
                      placeholder="데이터셋 설명"
                    />
                    <span class="form-text text-muted"
                      >Please enter dataset description.</span
                    >
                  </div>
                </div>
                <!--end: Wizard Step 1-->

                <!--begin: Wizard Step 2-->
                <div class="pb-5" data-wizard-type="step-content">
                  <h4 class="mb-10 font-weight-bold text-dark">
                    데이터 파일 업로드
                  </h4>
                  <div class="row mb-10 px-6">
                    <p>
                      데이터 세트를 만든 후에는 해당 파일이 기본 Blob Storage에
                      업로드되고 작업 영역에서 사용할 수 있게 됩니다. 지원되는
                      파일 형식으로는 구분된 파일 형식으로는 구분된 형식(즉 CSV,
                      TSV), Parquet, JSON 줄, 일반 텍스트 등이 있습니다.
                    </p>
                  </div>
                  <div class="form-group">
                    <label>데이터셋 업로드 *</label>
                    <input
                      type="file"
                      class="form-control form-control-solid form-control-lg"
                      name="fname"
                      placeholder="데이터셋 선택해주세요."
                    />
                    <span class="form-text text-muted"
                      >Please enter dataset file.</span
                    >
                  </div>
                </div>
                <!--end: Wizard Step 2-->

                <div class="pb-5" data-wizard-type="step-content">
                  <h4 class="mb-10 font-weight-bold text-dark">
                    세부정보 확인
                  </h4>
                  <div class="border-bottom mb-5 pb-5">
                    <div class="font-weight-bold mb-3">
                      <h4>이름:</h4>
                    </div>
                    <div class="line-height-md">
                      테스트 데이터
                    </div>
                  </div>
                  <div class="border-bottom mb-5 pb-5">
                    <div class="font-weight-bold mb-3">
                      <h4>설명:</h4>
                    </div>
                    <div class="line-height-md">
                      private portal 테스트를 위한 데이터 입니다.
                    </div>
                  </div>
                  <div class="mb-5 pb-5">
                    <div class="font-size-lg font-weight-bold mb-3">
                      <h4>업로드 파일:</h4>
                    </div>
                    <div class="line-height-md">
                      SKGC_Data_Test_200913_v0.1.XLS
                      <br />
                      SKGC_Data_Test_200913_v0.2.XLS
                      <br />
                      SKGC_Data_Test_200913_v0.3.XLS
                      <br />
                      SKGC_Data_Test_200913_v0.4.XLS
                    </div>
                  </div>
                </div>

                <!--begin: Wizard Step 4-->
                <div class="pb-5" data-wizard-type="step-content">
                  <h4 class="mb-10 font-weight-bold text-dark">
                    Setup Your Delivery Location
                  </h4>
                  <div class="row">
                    <div class="col-xl-6">
                      <div class="form-group">
                        <label>Address Line 1</label>
                        <input
                          type="text"
                          class="form-control form-control-solid form-control-lg"
                          name="locaddress1"
                          placeholder="Address Line 1"
                          value="Address Line 1"
                        />
                        <span class="form-text text-muted"
                          >Please enter your Address.</span
                        >
                      </div>
                    </div>
                    <div class="col-xl-6">
                      <div class="form-group">
                        <label>Address Line 2</label>
                        <input
                          type="text"
                          class="form-control form-control-solid form-control-lg"
                          name="locaddress2"
                          placeholder="Address Line 2"
                          value="Address Line 2"
                        />
                        <span class="form-text text-muted"
                          >Please enter your Address.</span
                        >
                      </div>
                    </div>
                  </div>
                  <div class="row">
                    <div class="col-xl-6">
                      <div class="form-group">
                        <label>Postcode</label>
                        <input
                          type="text"
                          class="form-control form-control-solid form-control-lg"
                          name="locpostcode"
                          placeholder="Postcode"
                          value="3072"
                        />
                        <span class="form-text text-muted"
                          >Please enter your Postcode.</span
                        >
                      </div>
                    </div>
                    <div class="col-xl-6">
                      <div class="form-group">
                        <label>City</label>
                        <input
                          type="text"
                          class="form-control form-control-solid form-control-lg"
                          name="loccity"
                          placeholder="City"
                          value="Preston"
                        />
                        <span class="form-text text-muted"
                          >Please enter your City.</span
                        >
                      </div>
                    </div>
                  </div>
                  <div class="row">
                    <div class="col-xl-6">
                      <div class="form-group">
                        <label>State</label>
                        <input
                          type="text"
                          class="form-control form-control-solid form-control-lg"
                          name="locstate"
                          placeholder="State"
                          value="VIC"
                        />
                        <span class="form-text text-muted"
                          >Please enter your state.</span
                        >
                      </div>
                    </div>
                    <div class="col-xl-6">
                      <div class="form-group">
                        <label>Country</label>
                        <select
                          name="loccountry"
                          class="form-control form-control-solid form-control-lg"
                        >
                          <option value="">Select</option>
                          <option value="AF">Afghanistan</option>
                          <option value="AX">Åland Islands</option>
                          <option value="AL">Albania</option>
                          <option value="DZ">Algeria</option>
                          <option value="AS">American Samoa</option>
                          <option value="AD">Andorra</option>
                        </select>
                      </div>
                    </div>
                  </div>
                </div>
                <!--end: Wizard Step 4-->

                <!--begin: Wizard Step 5-->
                <div class="pb-5" data-wizard-type="step-content">
                  <h4 class="mb-10 font-weight-bold text-dark">
                    Enter your Payment Details
                  </h4>
                  <div class="row">
                    <div class="col-xl-6">
                      <div class="form-group">
                        <label>Name on Card</label>
                        <input
                          type="text"
                          class="form-control form-control-solid form-control-lg"
                          name="ccname"
                          placeholder="Card Name"
                          value="John Wick"
                        />
                        <span class="form-text text-muted"
                          >Please enter your Card Name.</span
                        >
                      </div>
                    </div>
                    <div class="col-xl-6">
                      <div class="form-group">
                        <label>Card Number</label>
                        <input
                          type="text"
                          class="form-control form-control-solid form-control-lg"
                          name="ccnumber"
                          placeholder="Card Number"
                          value="4444 3333 2222 1111"
                        />
                        <span class="form-text text-muted"
                          >Please enter your Address.</span
                        >
                      </div>
                    </div>
                  </div>
                  <div class="row">
                    <div class="col-xl-4">
                      <div class="form-group">
                        <label>Card Expiry Month</label>
                        <input
                          type="number"
                          class="form-control form-control-solid form-control-lg"
                          name="ccmonth"
                          placeholder="Card Expiry Month"
                          value="01"
                        />
                        <span class="form-text text-muted"
                          >Please enter your Card Expiry Month.</span
                        >
                      </div>
                    </div>
                    <div class="col-xl-4">
                      <div class="form-group">
                        <label>Card Expiry Year</label>
                        <input
                          type="number"
                          class="form-control form-control-solid form-control-lg"
                          name="ccyear"
                          placeholder="Card Expire Year"
                          value="21"
                        />
                        <span class="form-text text-muted"
                          >Please enter your Card Expiry Year.</span
                        >
                      </div>
                    </div>
                    <div class="col-xl-4">
                      <div class="form-group">
                        <label>Card CVV Number</label>
                        <input
                          type="password"
                          class="form-control form-control-solid form-control-lg"
                          name="cccvv"
                          placeholder="Card CVV Number"
                          value="123"
                        />
                        <span class="form-text text-muted"
                          >Please enter your Card CVV Number.</span
                        >
                      </div>
                    </div>
                  </div>
                </div>
                <!--end: Wizard Step 5-->

                <!--begin: Wizard Step 6-->
                <div class="pb-5" data-wizard-type="step-content">
                  <h4 class="mb-10 font-weight-bold text-dark">
                    Review your Details and Submit
                  </h4>
                  <div class="border-bottom mb-5 pb-5">
                    <div class="font-weight-bold mb-3">
                      Account Details:
                    </div>
                    <div class="line-height-md">
                      John Wick
                      <br />
                      Phone: +61412345678 <br />
                      Email: johnwick@reeves.com
                    </div>
                  </div>
                  <div class="border-bottom mb-5 pb-5">
                    <div class="font-weight-bold mb-3">
                      Support Location Address:
                    </div>
                    <div class="line-height-md">
                      Address Line 1
                      <br />
                      Address Line 2 <br />
                      Melbourne 3000, VIC, Australia
                    </div>
                  </div>
                  <div class="border-bottom mb-5 pb-5">
                    <div class="font-weight-bold mb-3">
                      Support Channels:
                    </div>
                    <div class="line-height-md">
                      Overnight Delivery with Regular Packaging
                      <br />
                      Preferred Morning (8:00AM - 11:00AM) Delivery
                    </div>
                  </div>
                  <div class="border-bottom mb-5 pb-5">
                    <div class="font-weight-bold mb-3">
                      Delivery Address:
                    </div>
                    <div class="line-height-md">
                      Address Line 1:
                      <br />
                      Address Line 2 <br />
                      Preston 3072, VIC, Australia
                    </div>
                  </div>
                  <div class="mb-5">
                    <div class="font-weight-bold mb-3">
                      Payment Details:
                    </div>
                    <div class="line-height-md">
                      Card Number: xxxx xxxx xxxx 1111
                      <br />
                      Card Name: John Wick <br />
                      Card Expiry: 01/21
                    </div>
                  </div>
                </div>
                <!--end: Wizard Step 6-->

                <!--begin: Wizard Actions -->
                <div class="d-flex justify-content-between border-top pt-10">
                  <div class="mr-2">
                    <button
                      class="btn btn-light-primary font-weight-bold text-uppercase px-9 py-4"
                      data-wizard-type="action-prev"
                    >
                      Previous
                    </button>
                  </div>
                  <div>
                    <button
                      v-on:click="submit"
                      class="btn btn-success font-weight-bold text-uppercase px-9 py-4"
                      data-wizard-type="action-submit"
                    >
                      Submit
                    </button>
                    <button
                      class="btn btn-primary font-weight-bold text-uppercase px-9 py-4"
                      data-wizard-type="action-next"
                    >
                      Next Step
                    </button>
                  </div>
                </div>
                <!--end: Wizard Actions -->
              </form>
            </div>
            <!--end: Wizard-->
          </div>
        </div>
        <!--end: Wizard Body -->
      </div>
      <!--end: Wizard-->
    </div>
  </div>
</template>

<style lang="scss">
@import "@/assets/sass/pages/wizard/wizard-2.scss";
</style>

<script>
import { SET_BREADCRUMB } from "@/core/services/store/breadcrumbs.module";
import KTUtil from "@/assets/js/components/util";
import KTWizard from "@/assets/js/components/wizard";
import Swal from "sweetalert2";

export default {
  name: "Wizard-2",
  mounted() {
    this.$store.dispatch(SET_BREADCRUMB, [
      { title: "upload" },
      { title: "Data" }
    ]);

    // Initialize form wizard
    const wizard = new KTWizard("kt_wizard_v2", {
      startStep: 1, // initial active step number
      clickableSteps: true // allow step clicking
    });

    // Validation before going to next page
    wizard.on("beforeNext", function(/*wizardObj*/) {
      // validate the form and use below function to stop the wizard's step
      // wizardObj.stop();
    });

    // Change event
    wizard.on("change", function(/*wizardObj*/) {
      setTimeout(() => {
        KTUtil.scrollTop();
      }, 500);
    });
  },
  methods: {
    submit: function(e) {
      e.preventDefault();
      Swal.fire({
        title: "",
        text: "The application has been successfully submitted!",
        icon: "success",
        confirmButtonClass: "btn btn-secondary"
      });
    }
  }
};
</script>
