<template>
  <div>
    <Chart :cdata="cdata" />
  </div>
</template>

<script>
import Chart from './chart.vue';
export default {
  data () {
    return {
      cdata: {
        xData: ["类型一", "类型二", "类型三", "类型四", "类型五"],
        seriesData: [
          { value: 10, name: "类型一" },
          { value: 5, name: "类型二" },
          { value: 15, name: "类型三" },
          { value: 25, name: "类型四" },
          { value: 20, name: "类型五" },
        ]
      }
    }
  },
  components: {
    Chart,
  },
  mounted () {
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
</style>