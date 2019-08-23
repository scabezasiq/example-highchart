<template>
  <highcharts :options="chartOptions" class="map"></highcharts>
</template>

<script>

export default {
  data () {
    return {
      chartOptions: {
        chart: {
          type: 'column',
          inverted: true,
          padding: 0,
          backgroundColor: 'rgba(255, 255, 255, 0.0)',
          alignTicks: false,
        },
        title: {
          text: null,
        },
        subtitle: {
          text: null,
        },
        xAxis: {
          categories: ['Factor de Avance'],
          lineWidth: 0,
          tickWidth: 0,
          tickInterval: 1,
          labels: {
            enabled: false,
          },
        },
        yAxis: {
          title: false,
          lineWidth: 0,
          tickWidth: 0,
          minorTickInterval: 0.1,
          gridLineWidth: 0,
          minorGridLineWidth: 0,
          labels: {
            enabled: false,
          },
          min: 0,
          max: 100,
          isDirty: true,
        },
        plotOptions: {
          series: {
            marker: {
              enabled: false,
            },
          },
          column: {
            grouping: false,
            shadow: false,
            borderWidth: 0,
            borderRadius: 2,
          },
        },
        series: [
          {
            name: '1',
            color: 'rgba(255, 255, 255, 0.0)',
            borderColor: 'blue',
            borderWidth: 1,
            data: [100],
            pointPadding: 0.2,
          },
          {
            name: '2',
            color: 'red',
            data: [50],
            pointPadding: 0.415,
            pointPlacement: -0.08,
          },
          {
            name: '3',
            color: 'black',
            data: [70],
            pointPadding: 0.415,
            pointPlacement: 0.065,
          },
        ],
      }
    }
  }
}
</script>
 <style scoped>
.map {
  min-height: 500px;
}
 </style>
