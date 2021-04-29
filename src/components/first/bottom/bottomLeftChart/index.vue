<template>
  <div>
    <Chart :cdata="cdata" />
  </div>
</template>

<script>
import Chart from "./chart.vue";
export default {
  data() {
    return {
      cdata: {
        category: ["萧山区", "滨江区", "西湖区", "余杭区", "富阳区", "下沙区", "临平区"],
        lineData: [60, 98, 68, 98, 65, 75, 98],
        barData: [98, 75, 75, 65, 98, 75, 65],
        rateData: [],
      },
    };
  },
  components: {
    Chart,
  },
  mounted() {
    this.setData();
  },
  methods: {
    // 根据自己的业务情况修改
    setData() {
      for (let i = 0; i < this.cdata.barData.length - 1; i++) {
        let rate = this.cdata.barData[i] / this.cdata.lineData[i];
        this.cdata.rateData.push(rate.toFixed(2));
      }
    },
  },
};
</script>

<style lang="scss" scoped>
</style>