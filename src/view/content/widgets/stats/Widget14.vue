<template>
  <!--begin::Mixed Widget 14-->
  <div class="card card-custom gutter-b">
    <!--begin::Header-->
    <!-- <div class="card-header border-0 pt-5">
      <h2 class="card-title font-weight-bolder">
        {{ title }}
      </h2>
    </div> -->
    <!--end::Header-->
    <!--begin::Body-->
    <div class="card-body d-flex flex-column">
      <div>
        <div class="text-center p-3 border rounded bg-success text-white">
          <h3>{{ subTitle }}</h3>
          <h3>{{ count }}</h3>
        </div>
        <div
          v-html="description"
          class="text-center font-weight-bolder font-size-lg p-5 pre-formatted"
        ></div>
        <div class="w-100 text-center">
          <router-link to="/data/upload" v-slot="{ href }">
            <a
              :href="href"
              class="btn btn-primary btn-shadow-hover font-weight-bolder py-3 px-7 m-1"
              >{{ btnText }}</a
            >
          </router-link>
          <router-link to="/data/mng" v-slot="{ href }">
            <a
              :href="href"
              class="btn btn-primary btn-shadow-hover font-weight-bolder py-3 px-7 m-1"
              >{{ btnText2 }}</a
            >
          </router-link>
        </div>
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
  props: ["title", "desc", "btnText", "btnText2", "subTitle", "count"],
  computed: {
    ...mapGetters(["layoutConfig"]),
    description: function() {
      const desc = this.desc;
      return desc.replace(/(\\r)*\\n/g, "<br>");
    }
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
              fontSize: "30px",
              fontWeight: "700",
              offsetY: 12,
              show: true
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

<style scoped>
.pre-formatted {
  white-space: pre;
}
</style>
