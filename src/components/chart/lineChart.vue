<template>
  <div>
    <canvas id="myChart" width="400" height="400"></canvas>
  </div>
</template>

<script>
  import Chart from "chart.js";

  export default {
    name: "lineChart",
    mounted() {
      // console.log('chart is mounted');

      const ctx = document.getElementById('myChart');

      const myChart = new Chart(ctx, {
        type: 'line',
        data: {
          labels: ['', 'MON', 'TUE', 'WED', 'THU', 'FRI', 'SAT', 'SUN', ''],
          datasets: [{
            data: [0, 5, 8, 5, 9, 8, 10 , 15], 
            fill: false,
            borderColor: '#2FCA72',
            tension: 0
          }]
        },

        options: {
          bezierCurve : false,
          tooltips: {
            enabled: true,
            callbacks: {
              label: this.labelTooltip,
            }
          },

          legend: {
            display: false,
          },

          responsive: true,
          maintainAspectRatio: false,

          scales: {
            xAxes: [{
              ticks: {
                fontColor: "#8C8CA1",
                fontSize: 12,
              }
            }],

            yAxes: [{
              ticks: {
                fontColor: "#8C8CA1",
                fontSize: 12,
                max: 20,
                min: 0,
                stepSize: 5,
                callback: function (value) {
                  return '$' + value + 'K';
                },
              }
            }],
          }
        },
      });

      this.myChart = myChart;
    },

    methods: {
      labelTooltip(tooltipItems) {
        return 'Total Sales Overview $' + tooltipItems.yLabel + 'K';
      }
    }
  }
</script>

<style>
  /* @import "./lineChart.js"; */
  canvas {
    /* width: 1250px !important; */
    width: 1250px !important;
    height: 280px !important;
    margin-top: 30px;
    padding-left: 20px;
  }
</style>