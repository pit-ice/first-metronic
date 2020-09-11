<template>
  <!--begin::List Widget 9-->
  <div class="card card-custom gutter-b">
    <!--begin::Header-->
    <div class="card-header align-items-center border-0 mt-4">
      <h3 class="card-title align-items-start flex-column">
        <span class="font-weight-bolder text-dark">
          Project Activity
        </span>
        <span class="text-muted mt-3 font-weight-bold font-size-sm">
          24 Activity
        </span>
      </h3>
      <div class="card-toolbar">
        <Dropdown2></Dropdown2>
      </div>
    </div>
    <!--end::Header-->

    <!--begin::Body-->
    <div class="card-body pt-4">
      <div class="timeline timeline-6 mt-3">
        <template v-for="(item, i) in list">
          <!--begin::Item-->
          <div class="timeline-item align-items-start" v-bind:key="i">
            <!--begin::Label-->
            <div
              class="timeline-label font-weight-bolder text-dark-75 font-size-lg"
            >
              {{ item.time }}
            </div>
            <!--end::Label-->

            <!--begin::Badge-->
            <div class="timeline-badge">
              <i class="icon-xl" v-bind:class="item.badge"></i>
            </div>
            <!--end::Badge-->

            <!--begin::Text-->
            <div
              class="font-weight-mormal font-size-lg timeline-content text-muted pl-3"
            >
              <span
                v-bind:class="{
                  'font-weight-bolder text-dark-75': item.bold,
                  'mr-4': item.images
                }"
                v-html="item.desc"
              ></span>
            </div>
            <!--end::Text-->
          </div>
          <!--end::Item-->
        </template>
      </div>
      <!--end: Items-->
    </div>
    <!--end: Card Body-->
  </div>
  <!--end: Card-->
  <!--end: List Widget 9-->
</template>

<script>
import Dropdown2 from "@/view/content/dropdown/Dropdown2.vue";
import { mapGetters } from "vuex";

export default {
  name: "widget-9",
  data() {
    return {
      list: [
        {
          time: "08:42",
          desc: "이정원님이 R&D 노트를 등록하였습니다.",
          badge: "fa fa-genderless text-success"
        },
        {
          time: "10:00",
          desc: "홍길동님이 [팀원] 이정원을 추가하였습니다.",
          bold: true,
          badge: "fa fa-genderless text-danger"
        },
        {
          time: "14:37",
          desc: `홍길동님이 R&D 노트를 등록하였습니다.`,
          badge: "fa fa-genderless text-info",
          bold: true
        },
        {
          time: "16:50",
          desc: "홍길동님이 [모델] R&D Test Model 을 배포하였습니다.",
          badge: "fa fa-genderless text-danger"
        },
        {
          time: "17:30",
          desc: "김철수님이 R&D 노트를 등록하였습니다.",
          badge: "fa fa-genderless text-success",
          bold: true
        },
        {
          time: "21:03",
          desc: `김철수님이 [Data] R&D Test에 대한 [모델학습] R&D Test Model을 진행하였습니다.`,
          badge: "fa fa-genderless text-warning"
        },
        {
          time: "21:07",
          desc: "김철수님이 [Data] R&D Test를 등록하였습니다.",
          badge: "fa fa-genderless text-danger"
        },
        {
          time: "20:30",
          desc: "홍길동님이 Project를 생성하였습니다.",
          badge: "fa fa-genderless text-info",
          bold: true
        }
      ]
    };
  },
  components: {
    Dropdown2
  },
  methods: {
    lastElement(i) {
      if (i === this.list.length - 1) {
        return false;
      } else {
        return true;
      }
    }
  },
  computed: {
    ...mapGetters(["layoutConfig"])
  }
};
</script>
