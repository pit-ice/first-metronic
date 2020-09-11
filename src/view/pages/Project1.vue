<template>
  <div>
    <b-tabs content-class="mt-3">
      <b-tab title="Project Home" active>
        <!--begin::Dashboard-->
        <div class="row">
          <div class="col-xxl-3">
            <StatsWidget14
              title="데이터 등록하기"
              desc="모델학습에 이용할 데이터를 \n 등록합니다."
              btnText="등록하기"
              btnText2="관리하기"
              subTitle="데이터 등록 수"
              count="4"
            ></StatsWidget14>
          </div>
          <div class="col-xxl-3 ">
            <StatsWidget14
              title="모델 학습"
              desc="등록한 데이터를 이용하여 모델을\n 학습합니다."
              btnText="학습하기"
              btnText2="관리하기"
              subTitle="학습한 모델"
              count="3"
            ></StatsWidget14>
          </div>
          <div class="col-xxl-3 ">
            <StatsWidget14
              title="모델 배포"
              desc="학습한 모델을 선정하여\n 배포합니다."
              btnText="배포하기"
              btnText2="관리하기"
              subTitle="배포중인 모델"
              count="2"
            ></StatsWidget14>
          </div>
          <div class="col-xxl-3 ">
            <StatsWidget14
              title="모델 시뮬레이션"
              desc="배포한 모델을 이용하여 시뮬레이션\n 합니다."
              btnText="시뮬레이션"
              btnText2="결과조회"
              subTitle="시뮬레이션 횟수"
              count="5"
            ></StatsWidget14>
          </div>
          <div class="col-xxl-8">
            <AdvancedTableWidget4></AdvancedTableWidget4>
          </div>
          <div class="col-xxl-4 ">
            <ListWidget10></ListWidget10>
            <StatsWidget13></StatsWidget13>
          </div>
        </div>
        <!--end::Dashboard-->
      </b-tab>
      <b-tab title="Data Mgmt"></b-tab>
      <b-tab title="Model Mgmt"></b-tab>
      <b-tab title="Simulation"></b-tab>
      <b-tab title="Member"></b-tab>
      <b-tab title="연구노트"></b-tab>
    </b-tabs>
  </div>
</template>

<script>
import { SET_BREADCRUMB } from "@/core/services/store/breadcrumbs.module";
import AdvancedTableWidget4 from "@/view/content/widgets/advance-table/Widget4.vue";
import ListWidget10 from "@/view/content/widgets/list/Widget10.vue";
import StatsWidget13 from "@/view/content/widgets/stats/Widget13.vue";
import StatsWidget14 from "@/view/content/widgets/stats/Widget14.vue";

export default {
  name: "dashboard",
  components: {
    AdvancedTableWidget4,
    ListWidget10,
    StatsWidget13,
    StatsWidget14
  },
  mounted() {
    this.$store.dispatch(SET_BREADCRUMB, [
      { title: "PROJECT" },
      { title: "Skgc 범퍼 개발" }
    ]);
  },
  methods: {
    setActiveTab1(event) {
      this.tabIndex = this.setActiveTab(event);
    },
    setActiveTab2(event) {
      this.tabIndex2 = this.setActiveTab(event);
    },
    /**
     * Set current active on click
     * @param event
     */
    setActiveTab(event) {
      // get all tab links
      const tab = event.target.closest('[role="tablist"]');
      const links = tab.querySelectorAll(".nav-link");
      // remove active tab links
      for (let i = 0; i < links.length; i++) {
        links[i].classList.remove("active");
      }

      // set current active tab
      event.target.classList.add("active");

      // set clicked tab index to bootstrap tab
      return parseInt(event.target.getAttribute("data-tab"));
    }
  }
};
</script>
