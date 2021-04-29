<template>
  <div id="centreRight2">
    <div class="bg-color-black">
      <div class="d-flex pt-2 pl-2">
        <span style="color: #5cd9e8">
          <icon name="align-left"></icon>
        </span>
        <span class="fs-xl text mx-2">疾病分析</span>
      </div>
      <div
        class="d-flex jc-center body-box"
        style="
          margin-top: 0.1rem;
          display: grid;
          grid-template-columns: 2fr 2fr 2fr 2fr;
          color: #1a5cd7;
        "
      >
        <div style="text-align: center">
          疾病名称
          <div
            v-for="item in this.illNameList"
            :key="item.id"
            style="color: #fff; margin: 0.2rem"
          >
            {{ item.name }}
          </div>
        </div>
        <div style="text-align: center">
          查看总次数
          <div
            v-for="item in this.totalList"
            :key="item.id"
            style="color: #fff; margin: 0.2rem"
          >
            {{ item.name }}
          </div>
        </div>
        <div style="text-align: center">
          查看总人数
          <div
            v-for="item in this.totalList"
            :key="item.id"
            style="color: #fff; margin: 0.2rem"
          >
            {{ item.name }}
          </div>
        </div>
        <div style="text-align: center;color:#F56C6C;">
          平均停留时间
          <div
            v-for="item in this.totalList"
            :key="item.id"
            style="color: #fff; margin: 0.2rem"
          >
            {{ item.name }}
          </div>
        </div>
        <!-- <dv-capsule-chart :config="config" style="width: 100%;height:2rem" /> -->
        <!-- <centreRight2Chart1 /> -->
      </div>
    </div>
  </div>
</template>

<script>
// import centreRight2Chart1 from "@/components/first/centerRight/centerRightChart";

export default {
  data() {
    return {
      illNameList: [
        { name: "高血压", id: 1 },
        { name: "糖尿病", id: 2 },
        { name: "慢阻肺病", id: 3 },
        { name: "脑梗", id: 4 },
        { name: "脑卒中", id: 5 },
        { name: "心肌", id: 6 },
        { name: "慢性心脏病", id: 7 },
        { name: "乙肝", id: 8 },
        { name: "肺癌", id: 9 },
        { name: "子宫癌", id: 10 },
        { name: "天花", id: 11 },
      ],
      totalList: [
        { name: "10", id: 1 },
        { name: "36", id: 2 },
        { name: "56", id: 3 },
        { name: "76", id: 4 },
        { name: "86", id: 5 },
        { name: "96", id: 6 },
        { name: "95", id: 7 },
        { name: "106", id: 8 },
        { name: "121", id: 9 },
        { name: "65", id: 10 },
        { name: "56", id: 11 },
      ],
      config: {
        data: [
          {
            name: "南阳",
            value: 167,
          },
          {
            name: "周口",
            value: 67,
          },
          {
            name: "漯河",
            value: 123,
          },
          {
            name: "郑州",
            value: 55,
          },
          {
            name: "西峡",
            value: 98,
          },
        ],
      },
    };
  },
  // components: { centreRight2Chart1 },
  mounted() {},
  methods: {},
};
</script>

<style lang="scss">
#centreRight2 {
  padding: 0.0625rem;
  height: 5rem;
  // min-width: 3.75rem;
  width: 100%;
  border-radius: 0.0625rem;
  .bg-color-black {
    padding: 0.0625rem;
    height: 5.0625rem;
    border-radius: 0.125rem;
  }
  .text {
    color: #c3cbde;
  }
  .body-box {
    border-radius: 0.125rem;
    overflow: hidden;
  }
}
</style>