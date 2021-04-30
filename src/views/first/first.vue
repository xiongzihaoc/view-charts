<template>
  <div id="index">
    <dv-full-screen-container class="bg">
      <dv-loading v-if="loading">Loading...</dv-loading>
      <div v-else class="host-body">
        <div class="d-flex jc-center">
          <dv-decoration-10 style="width: 33.3%; height: 0.0625rem" />
          <div class="d-flex jc-center">
            <dv-decoration-8
              :color="['#568aea', '#000000']"
              style="width: 2.5rem; height: 0.625rem"
            />
            <div class="title">
              <span class="title-text">老年人数字健康管理中心</span>
            </div>
            <dv-decoration-8
              :reverse="true"
              :color="['#568aea', '#000000']"
              style="width: 2.5rem; height: 0.625rem"
            />
          </div>
          <dv-decoration-10
            style="width: 33.3%; height: 0.0625rem; transform: rotateY(180deg)"
          />
        </div>

        <!-- 第二行 -->
        <div class="d-flex jc-between px-2">
          <div class="d-flex" style="width: 40%">
            <div class="react-right ml-3 bg-color-blue">
              <span class="text fw-b">{{
                titleList[0].name + titleList[0].value
              }}</span>
            </div>
            <div class="react-right ml-3 bg-color-blue">
              <span class="text fw-b">{{
                titleList[1].name + titleList[1].value
              }}</span>
            </div>
            <div class="react-right ml-3 bg-color-blue">
              <span class="text fw-b">{{
                titleList[2].name + titleList[2].value
              }}</span>
            </div>
            <div class="react-right ml-3 bg-color-blue">
              <span class="text fw-b">{{
                titleList[3].name + titleList[3].value
              }}</span>
            </div>
          </div>
          <div style="width: 40%" class="d-flex">
            <div class="react-left bg-color-blue mr-3">
              <span class="text fw-b">{{
                titleList[4].name + titleList[4].value
              }}</span>
            </div>
            <div class="react-left bg-color-blue mr-3">
              <span class="text fw-b">{{
                titleList[5].name + titleList[5].value
              }}</span>
            </div>
            <div class="react-left bg-color-blue mr-3">
              <span class="text fw-b">{{
                titleList[6].name + titleList[6].value
              }}</span>
            </div>
          </div>
        </div>

        <div class="body-box">
          <!-- 第三行数据 -->
          <div class="content-box">
            <div>
              <dv-border-box-12>
                <centerLeft1 />
              </dv-border-box-12>
            </div>
            <div>
              <dv-border-box-12>
                <centerLeft2 />
              </dv-border-box-12>
            </div>
            <!-- 中间 -->
            <div>
              <dv-border-box-11 title="慢性病下降率 TOP10"
                ><center
              /></dv-border-box-11>
            </div>
            <!-- 中间 -->
            <div>
              <dv-border-box-1> <centerRight2 /></dv-border-box-1>
            </div>
          </div>

          <!-- 第四行数据 -->
          <div class="bototm-box">
            <dv-border-box-13>
              <bottomLeft />
            </dv-border-box-13>
            <dv-border-box-12>
              <bottomRight />
              <!-- <dv-flyline-chart
                :relative="false"
                :config="flylineConfig"
                style="width: 100%; height: 100%"
              /> -->
            </dv-border-box-12>
          </div>
        </div>
      </div>
    </dv-full-screen-container>
  </div>
</template>

<script>
// import { formatTime } from "../../utils/index.js";
import centerLeft1 from "./centerLeft1";
import centerLeft2 from "./centerLeft2";
// import centerRight1 from "./centerRight1";
import centerRight2 from "./centerRight2";
import center from "./center";
import bottomLeft from "./bottomLeft";
// import JSON from '../../common/map/hangzhou.json'
import bottomRight from "./bottomRight";
export default {
  data() {
    return {
      loading: true,
      titleList: [
        { name: "血压控制率", value: "80%" },
        { name: "血糖控制率", value: "70%" },
        { name: "家医签约率", value: "90%" },
        { name: "家医随访率", value: "90%" },
        { name: "中医院管理率", value: "80%" },
        { name: "高血压管理率", value: "70%" },
        { name: "糖尿病管理率", value: "90%" },
      ],
      flylineConfig: {
        centerPoint: [0.48, 0.35],
        points: [
          {
            position: [0.52, 0.235],
            text: "新乡",
          },
          {
            position: [0.43, 0.29],
            text: "焦作",
          },
          {
            position: [0.59, 0.35],
            text: "开封",
          },
          {
            position: [0.53, 0.47],
            text: "许昌",
          },
          {
            position: [0.45, 0.54],
            text: "平顶山",
          },
          {
            position: [0.36, 0.38],
            text: "洛阳",
          },
          {
            position: [0.62, 0.55],
            text: "周口",
          },
          {
            position: [0.56, 0.56],
            text: "漯河",
          },
          {
            position: [0.37, 0.66],
            text: "南阳",
          },
          {
            position: [0.55, 0.81],
            text: "信阳",
          },
          {
            position: [0.55, 0.67],
            text: "驻马店",
          },
          {
            position: [0.37, 0.29],
            text: "济源",
          },
          {
            position: [0.2, 0.36],
            text: "三门峡",
          },
          {
            position: [0.76, 0.41],
            text: "商丘",
          },
          {
            position: [0.59, 0.18],
            text: "鹤壁",
          },
          {
            position: [0.68, 0.17],
            text: "濮阳",
          },
          {
            position: [0.59, 0.1],
            text: "安阳",
          },
        ],
        bgImgUrl: "/img/flylineChart/map.jpg",
        centerPointImg: {
          url: "/img/flylineChart/mapCenterPoint.png",
        },
        pointsImg: {
          url: "/img/flylineChart/mapPoint.png",
        },
      },
    };
  },
  components: {
    centerLeft1,
    centerLeft2,
    // centerRight1,
    centerRight2,
    center,
    bottomLeft,
    bottomRight,
  },
  mounted() {
    // this.timeFn();
    this.cancelLoading();
  },
  methods: {
    // timeFn() {
    //   setInterval(() => {
    //     this.dateDay = formatTime(new Date(), "HH: mm: ss");
    //     this.dateYear = formatTime(new Date(), "yyyy-MM-dd");
    //     this.dateWeek = this.weekday[new Date().getDay()];
    //   }, 1000);
    // },
    cancelLoading() {
      setTimeout(() => {
        this.loading = false;
      }, 500);
    },
  },
};
</script>

<style lang="scss">
@import "../../assets/scss/index.scss";
</style>