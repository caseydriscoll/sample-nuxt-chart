<template>
  <client-only>
    <div>
      <VueApexCharts
        width="500"
        :type="chart.type"
        :options="chart.options"
        :series="chart.series"
      ></VueApexCharts>
    </div>
  </client-only>
</template>

<script>
export default {
  components: {
    VueApexCharts: () => import('vue-apexcharts'),
  },
  props: {
    chart: {
      type: Object,
      required: true,
    },
  },
}
</script>
