<template>
  <div class="container">
    <el-table :data="tableData" style="width: 100%">
      <div v-for="(item, index) in tableTitle" :key="index">
        <el-table-column :prop="item.property" :label="item.label" width="180">
        </el-table-column>
        <!-- 插槽 -->
        <slot v-if="item.slot" name='handle'></slot>
      </div>
    </el-table>
  </div>
</template>

<script>
export default {
  name: "chris-el-table",
  props: {
    tableData: {
      type: Array,
      default: () => {
        return [];
      },
    },
    tableTitle: {
      type: Array,
      require: true,
    },
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
.container {
  margin-bottom: 20px;
}
/* 去掉表格底部边框 */
.container .el-table::before {
  background: none;
}

/* 表格hover效果 */
::v-deep
  .el-table--enable-row-hover
  .el-table__body
  tr:hover
  > td.el-table__cell {
  background-color: #a1b1c8;
}
/* 表头样式 */
::v-deep .el-table__header-wrapper .el-table__cell {
  height: 44px;
  padding: 0;
  background: #ded6d6;
  border-bottom: #ebeef5 solid 1px !important;
  text-align: center;
}

::v-deep .el-table__row .el-table__cell .cell{
    display: flex;
    justify-content: center;
}
</style>