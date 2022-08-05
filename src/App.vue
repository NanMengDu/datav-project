<template>
  <div id="app">
    <dv-loading>Loading...</dv-loading>
    <div class="dv">
      <dv-border-box-1></dv-border-box-1>
    </div>
    <dv-border-box-8></dv-border-box-8>
    <div class="dv">
      <dv-border-box-12></dv-border-box-12>
    </div>
    <div class="dv">
      <dv-border-box-13></dv-border-box-13>
    </div>
    <div class="dv">
      <dv-decoration-1 :color="['red', 'green']" />
    </div>
    <div class="dv">
      <dv-decoration-2 />
    </div>
    <!-- 组件 -->
    <chris-el-table :table-title="tableTitle" :table-data="tableData">
      <el-table-column slot="handle" label="操作" width="180">
        <template slot-scope="scope">
          <el-button @click="handleClick(scope.row)">查看</el-button>
        </template>
      </el-table-column>
    </chris-el-table>
      <!-- 图表 -->
    <myChart></myChart>
    <my-swiper></my-swiper>
  </div>
</template>

<script>
import ChrisElTable from "./components/chris-el-table.vue";
import myChart from './components/echarts.vue'
import mySwiper from './components/myswiper.vue'
export default {
  name: "App",
  components: { ChrisElTable,myChart,mySwiper },
  data() {
    return {
      tableTitle: [
        {
          label: "日期",
          property: "date",
        },
        {
          label: "姓名",
          property: "name",
        },
        {
          label: "地址",
          property: "address",
          slot:'handle'
        },
      ],
      tableData: [
        {
          date: "2016-05-02",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1518 弄",
        },
        {
          date: "2016-05-04",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1517 弄",
        },
        {
          date: "2016-05-01",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1519 弄",
        },
        {
          date: "2016-05-03",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1516 弄",
        },
      ],
    };
  },
  methods:{
    handleClick(row){
        console.log(row);
    }
  }
};

</script>

<style>
#app {
  width: 90vw;
}
#app .dv-border-box-8 {
  width: 300px;
  height: 300px;
  margin: 20px;
}
.dv .dv-border-box-1,
.dv .dv-border-box-12,
.dv .dv-border-box-13,
.dv .dv-decoration-2 {
  width: 300px;
  height: 300px;
  margin: 20px;
}
</style>
