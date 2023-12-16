<!-- LineChart.vue -->
<template>
  <div class="line-chart">
    <canvas ref="lineChartCanvas"></canvas>
  </div>
</template>

<script>
import Chart from "chart.js";

export default {
  name: "LineChart",
  data() {
    return {
      chartData: {
        labels: ["Jan", "Feb", "Mar"],
        datasets: [
          {
            label: "Monthly Performance",
            data: [10, 20, 15],
            borderColor: "rgba(75, 192, 192, 1)",
            borderWidth: 2,
            fill: false,
          },
        ],
      },
    };
  },
  mounted() {
    this.renderLineChart();
  },
  methods: {
    renderLineChart() {
      const ctx = this.$refs.lineChartCanvas.getContext("2d");
      new Chart(ctx, {
        type: "line",
        data: this.chartData,
        options: {
          scales: {
            y: {
              beginAtZero: true,
            },
          },
        },
      });
    },
  },
};
</script>

<style scoped>
.line-chart {
  width: 100%;
  height: 100%;
}
</style>
