<template>
  <!--begin::Advance Table Widget 9-->
  <div class="card card-custom card-stretch gutter-b">
    <!--begin::Header-->
    <div class="card-header border-0 py-5">
      <h3 class="card-title align-items-start flex-column">
        <span class="card-label font-weight-bolder text-dark">RnD Note</span>
        <span class="text-muted mt-3 font-weight-bold font-size-sm"
          >More than 400+ new notes</span
        >
      </h3>
      <div class="card-toolbar">
        <a href="#" class="btn btn-danger font-weight-bolder font-size-sm"
          >More</a
        >
      </div>
    </div>
    <!--end::Header-->
    <!--begin::Body-->
    <div class="card-body pt-0 pb-3">
      <div class="tab-content">
        <!--begin::Table-->
        <div class="table-responsive">
          <table
            class="table table-head-custom table-vertical-center table-head-bg table-borderless"
          >
            <thead>
              <tr class="text-left">
                <th style="min-width: 250px" class="pl-7">
                  <span class="text-dark-75">user</span>
                </th>
                <th style="min-width: 120px">
                  <span class="text-dark-75">title</span>
                </th>
                <th style="min-width: 120px">
                  <span class="text-dark-75">date</span>
                </th>
                <th style="min-width: 101px"></th>
              </tr>
            </thead>
            <tbody>
              <template v-for="(item, i) in list">
                <tr v-bind:key="i">
                  <td class="pl-0 pt-8">
                    <div class="d-flex align-items-center">
                      <div class="symbol symbol-50 symbol-light mr-4">
                        <span class="symbol-label">
                          <img
                            :src="item.img"
                            class="h-75 align-self-end"
                            alt=""
                          />
                        </span>
                      </div>
                      <div>
                        <a
                          href="#"
                          class="text-dark-75 font-weight-bolder text-hover-primary mb-1 font-size-lg"
                          >{{ item.name }}</a
                        >
                        <span class="text-muted font-weight-bold d-block">{{
                          item.desc
                        }}</span>
                      </div>
                    </div>
                  </td>
                  <td>
                    <span
                      class="text-dark-75 font-weight-bolder d-block font-size-lg"
                      >{{ item.title }}</span
                    >
                    <span class="text-muted font-weight-bold">{{
                      item.status
                    }}</span>
                  </td>
                  <td>
                    <span class="text-dark-75 d-block font-size-lg">
                      {{ item.date }}</span
                    >
                  </td>
                  <td class="pr-0 text-right">
                    <a
                      href="#"
                      class="btn btn-light-success font-weight-bolder font-size-sm"
                      >View</a
                    >
                  </td>
                </tr>
              </template>
            </tbody>
          </table>
        </div>
        <!--end::Table-->
      </div>
    </div>
    <!--end::Body-->
  </div>
  <!--end::Advance Table Widget 9-->
</template>

<script>
export default {
  name: "widget-3",
  data() {
    return {
      list: [
        {
          img: process.env.BASE_URL + "media/svg/avatars/001-boy.svg",
          name: "홍길동",
          desc: "SKGC - Developer",
          title: "모델 autooml-db_0321 분석 결과 공유합니다.",
          status: "Completed",
          status2: "Paid",
          date: "2020.08.31 16:00",
          amount: "$520",
          company: "Intertico",
          company_desc: "Web, UI/UX Design",
          rate: "Best Rated"
        },
        {
          img: process.env.BASE_URL + "media/svg/avatars/018-girl-9.svg",
          name: "김철수",
          desc: "SKGC - DataMng",
          paid: "$23,000,000",
          title: "모델 autooml-db_0321 분석 결과 공유합니다.",
          status: "Completed",
          status2: "Rejected",
          date: "2020.08.31 16:00",
          amount: "$1,600",
          company: "Agoda",
          company_desc: "Houses & Hotels",
          rate: "Above Average"
        },
        {
          img: process.env.BASE_URL + "media/svg/avatars/014-girl-7.svg",
          name: "Lebron Wayde",
          desc: "PHP, Laravel, VueJS",
          title: "모델 autooml-db_0321 분석 결과 공유합니다.",
          status: "Completed",
          status2: "Paid",
          date: "2020.08.31 16:00",
          amount: "$6,700",
          company: "RoadGee",
          company_desc: "Transportation",
          rate: "Best Rated"
        },
        {
          img: process.env.BASE_URL + "media/svg/avatars/047-girl-25.svg",
          name: "Natali Trump",
          desc: "Python, PostgreSQL",
          title: "모델 autooml-db_0321 분석 결과 공유합니다.",
          status: "Completed",
          status2: "Pending",
          date: "2020.08.31 16:00",
          amount: "$14,000",
          company: "The Hill",
          company_desc: "Insurance",
          rate: "Average"
        },
        {
          img: process.env.BASE_URL + "media/svg/avatars/001-boy.svg",
          name: "홍길동",
          desc: "SKGC - Developer",
          title: "모델 autooml-db_0321 분석 결과 공유합니다.",
          status: "Completed",
          status2: "Paid",
          date: "2020.08.31 16:00",
          amount: "$520",
          company: "Intertico",
          company_desc: "Web, UI/UX Design",
          rate: "Best Rated"
        },
        {
          img: process.env.BASE_URL + "media/svg/avatars/018-girl-9.svg",
          name: "김철수",
          desc: "SKGC - DataMng",
          paid: "$23,000,000",
          title: "모델 autooml-db_0321 분석 결과 공유합니다.",
          status: "Completed",
          status2: "Rejected",
          date: "2020.08.31 16:00",
          amount: "$1,600",
          company: "Agoda",
          company_desc: "Houses & Hotels",
          rate: "Above Average"
        },
        {
          img: process.env.BASE_URL + "media/svg/avatars/014-girl-7.svg",
          name: "Lebron Wayde",
          desc: "PHP, Laravel, VueJS",
          title: "모델 autooml-db_0321 분석 결과 공유합니다.",
          status: "Completed",
          status2: "Paid",
          date: "2020.08.31 16:00",
          amount: "$6,700",
          company: "RoadGee",
          company_desc: "Transportation",
          rate: "Best Rated"
        },
        {
          img: process.env.BASE_URL + "media/svg/avatars/047-girl-25.svg",
          name: "Natali Trump",
          desc: "Python, PostgreSQL",
          title: "모델 autooml-db_0321 분석 결과 공유합니다.",
          status: "Completed",
          status2: "Pending",
          date: "2020.08.31 16:00",
          amount: "$14,000",
          company: "The Hill",
          company_desc: "Insurance",
          rate: "Average"
        },
        {
          img: process.env.BASE_URL + "media/svg/avatars/014-girl-7.svg",
          name: "Lebron Wayde",
          desc: "PHP, Laravel, VueJS",
          title: "모델 autooml-db_0321 분석 결과 공유합니다.",
          status: "Completed",
          status2: "Paid",
          date: "2020.08.31 16:00",
          amount: "$6,700",
          company: "RoadGee",
          company_desc: "Transportation",
          rate: "Best Rated"
        }
      ]
    };
  }
};
</script>
