<template>
  <el-table
    :data="tableData"
    border
    :header-cell-style="{textAlign: 'center'}"
    :cell-style="{ textAlign: 'center' }"
    style="width: 100%">
    <el-table-column
      fixed
      prop="date"
      label="试验状态"
      algin="center"
      width="150">
      <el-tag>待打印</el-tag>
    </el-table-column>
    <el-table-column
      prop="name"
      label="判断结果"
      width="120"
    >
      <el-tag type="danger"  >未知状态</el-tag>
    </el-table-column>
    <el-table-column
      prop="province"
      label="委托编号"
      width="120">
    </el-table-column>
    <el-table-column
      prop="city"
      label="试验项目"
      width="120">
    </el-table-column>
    <el-table-column
      prop="address"
      label="委托日期"
      width="300">
    </el-table-column>
    <el-table-column
      prop="zip"
      label="试验类型"
      width="120">
    </el-table-column>
    <el-table-column
      fixed="right"
      label="委托单位"
      width="100">
      <template slot-scope="scope">
        <el-button @click="handleClick(scope.row)" type="text" size="small">查看</el-button>
        <el-button type="text" size="small">编辑</el-button>
      </template>
    </el-table-column>
  </el-table>
</template>

<script>
export default {
  name: "entrustTable",
  methods: {
    handleClick(row) {
      console.log(row);
    }
  },

  data() {
    return {
      tableData: [{
        date: '2016-05-02',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1518 弄',
        zip: 200333
      }, {
        date: '2016-05-04',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1517 弄',
        zip: 200333
      }, {
        date: '2016-05-01',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1519 弄',
        zip: 200333
      }, {
        date: '2016-05-03',
        name: '王小虎',
        province: '上海',
        city: '普陀区',
        address: '上海市普陀区金沙江路 1516 弄',
        zip: 200333
      }]
    }
  }
}
</script>

<style scoped>

</style>
