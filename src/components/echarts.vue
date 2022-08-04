<template>
  <div>
    <div id="main" style="width: 600px; height: 400px;border:1px solid;margin:10px"></div>
  </div>
</template>
<script>
import * as echarts from "echarts";
export default {
  mounted() {
    var chartDom = document.getElementById("main");
    var myChart = echarts.init(chartDom);
    var option = {
        // 配置title
        title:{ 
            text:'柱状图',
            // 指定跳转的连接
            link:'http://www.baidu.com',
            //默认是blank
            target:'self',
            // 标题样式
            textStyle:{
                color:'red',
                lineHeight:30,
                // 字体描边的样式
                textBorderWidth:'2',
                textBorderType:'solid',
                textBorderColor:'black'
            },
            subtextStyle:{
                color:'red',
                fontSize:30,
                verticalAlign:'top'
            }
        },
        // 显示隐藏图表
        legend:{
            // 图例样式
            icon:'circle',
            backgroundColor:'lightgreen',
            borderRadius:4
        },
      tooltip: {
        trigger: "axis",//item无类目轴的图表中使用
        // 指示器类型
        axisPointer: {
            //shadow 阴影指示器 line 直线指示器 cross 十字准星指示器
          type: "line",
        },
      },
      grid: {
        left: "3%",
        right: "4%",
        bottom: "3.5%",
        // grid 区域是否包含坐标轴的刻度标签
        containLabel: true,
        // 是否显示直角坐标系网格。
        show:true,
        // borderColor:'red'
      },
      xAxis: [
        {
          type: "category",
          data: ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"],
          axisTick: {
            alignWithLabel: true,
          },
        },
        
      ],
      yAxis: [
        {
          type: "value",
        },
      ],
      series: [
        {
          name: "图表",
          type: "bar",
          barWidth: "60%",
          data: [10, 52, 200, 334, 390, 330, 220],
        },
      ],
    };
    myChart.setOption(option);
  },
};
</script>