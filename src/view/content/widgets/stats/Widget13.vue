<template>
  <!--begin::Mixed Widget 14-->
  <div class="card card-custom gutter-b">
    <!--begin::Header-->
    <div class="card-header border-0 pt-5">
      <h3 class="card-title font-weight-bolder">학습 현황</h3>
      <div class="card-toolbar">
        <div class="dropdown dropdown-inline">
          <a
            href="#"
            class="btn btn-clean btn-sm btn-icon"
            data-toggle="dropdown"
            aria-haspopup="true"
            aria-expanded="false"
          >
            <i class="ki ki-bold-more-hor"></i>
          </a>
          <div class="dropdown-menu dropdown-menu-md dropdown-menu-right">
            <!--begin::Navigation-->
            <ul class="navi navi-hover py-5">
              <li class="navi-item">
                <a href="#" class="navi-link">
                  <span class="navi-icon">
                    <i class="flaticon2-drop"></i>
                  </span>
                  <span class="navi-text">New Group</span>
                </a>
              </li>
              <li class="navi-item">
                <a href="#" class="navi-link">
                  <span class="navi-icon">
                    <i class="flaticon2-list-3"></i>
                  </span>
                  <span class="navi-text">Contacts</span>
                </a>
              </li>
              <li class="navi-item">
                <a href="#" class="navi-link">
                  <span class="navi-icon">
                    <i class="flaticon2-rocket-1"></i>
                  </span>
                  <span class="navi-text">Groups</span>
                  <span class="navi-link-badge">
                    <span
                      class="label label-light-primary label-inline font-weight-bold"
                      >new</span
                    >
                  </span>
                </a>
              </li>
              <li class="navi-item">
                <a href="#" class="navi-link">
                  <span class="navi-icon">
                    <i class="flaticon2-bell-2"></i>
                  </span>
                  <span class="navi-text">Calls</span>
                </a>
              </li>
              <li class="navi-item">
                <a href="#" class="navi-link">
                  <span class="navi-icon">
                    <i class="flaticon2-gear"></i>
                  </span>
                  <span class="navi-text">Settings</span>
                </a>
              </li>
              <li class="navi-separator my-3"></li>
              <li class="navi-item">
                <a href="#" class="navi-link">
                  <span class="navi-icon">
                    <i class="flaticon2-magnifier-tool"></i>
                  </span>
                  <span class="navi-text">Help</span>
                </a>
              </li>
              <li class="navi-item">
                <a href="#" class="navi-link">
                  <span class="navi-icon">
                    <i class="flaticon2-bell-2"></i>
                  </span>
                  <span class="navi-text">Privacy</span>
                  <span class="navi-link-badge">
                    <span
                      class="label label-light-danger label-rounded font-weight-bold"
                      >5</span
                    >
                  </span>
                </a>
              </li>
            </ul>
            <!--end::Navigation-->
          </div>
        </div>
      </div>
    </div>
    <!--end::Header-->
    <!--begin::Body-->
    <div class="card-body d-flex flex-column">
      <div class="flex-grow-1">
        <apexchart
          :options="chartOptions"
          :series="series"
          type="radialBar"
        ></apexchart>
      </div>
      <div class="pt-5">
        <p class="text-center font-weight-normal font-size-lg pb-7">
          Notes : 학습이 완료되면, 학습 결과 조회 후 모델 배포를 진행할 수
          있습니다.
        </p>
        <a
          href="#"
          class="btn btn-success btn-shadow-hover font-weight-bolder w-100 py-3"
          >학습현황 바로가기</a
        >
      </div>
    </div>
    <!--end::Body-->
  </div>
  <!--end::Mixed Widget 14-->
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "widget-7",
  data() {
    return {
      chartOptions: {},
      series: [74]
    };
  },
  computed: {
    ...mapGetters(["layoutConfig"])
  },
  mounted() {
    // reference; kt_stats_widget_7_chart
    this.chartOptions = {
      chart: {
        height: 200,
        type: "radialBar"
      },
      plotOptions: {
        radialBar: {
          hollow: {
            margin: 0,
            size: "65%"
          },
          dataLabels: {
            showOn: "always",
            name: {
              show: false,
              fontWeight: "700"
            },
            value: {
              color: this.layoutConfig("colors.gray.gray-700"),
              fontSize: "20px",
              fontWeight: "500",
              offsetY: 10,
              show: true,
              formatter: function() {
                return "14:35";
              }
            }
          },
          track: {
            background: this.layoutConfig("colors.theme.light.success"),
            strokeWidth: "100%"
          }
        }
      },
      colors: [this.layoutConfig("colors.theme.base.success")],
      stroke: {
        lineCap: "round"
      },
      labels: ["Progress"]
    };
  }
};
</script>
