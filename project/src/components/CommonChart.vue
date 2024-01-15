<template>
    <div class="echart" id="mychart" :style="myChartStyle"></div>
  </template>
  
  <script>
  import * as echarts from "echarts";
  
  export default {
    data() {
      return {
        xData: ["上海", "北京", "浙江", "天津", "河北", "黑龙江", "内蒙古","广东","广西", "西安", "河南", "合肥", "乌鲁木齐", "上海", "北京","山东"], //横坐标
        yData: [23, 24, 18, 25, 27, 28, 25,12,23, 24, 18, 25, 27, 28, 25,12], //数据
        myChartStyle: { float: "left", width: "100%", height: "400px" } //图表样式
      };
    },
    mounted() {
      this.initEcharts();
    },
    methods: {
      initEcharts() {
        // 基本柱状图
        const option = {
          xAxis: {
            data: this.xData
          },
          yAxis: {type: 'value'},
          series: [
            {
              type: "bar", //形状为柱状图
              data: this.yData,
              datasetIndex: 1
            }
          ]
        };
        const myChart = echarts.init(document.getElementById("mychart"));
        myChart.setOption(option);
        //随着屏幕大小调节图表
        window.addEventListener("resize", () => {
          myChart.resize();
        });
      }
    }
  };
  </script>
  
  <style>
    .echart{
        margin-left: -100px;
    }
</style>