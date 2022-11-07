<template>
<div>

  <el-tabs v-model="activeName" @tab-click="handleClick" style="margin-left: 20px">
    <el-tab-pane label="全部台账" name="first">

      <el-row>
        <el-col :span="4"><div class="grid-content bg-purple">
          <el-input v-model="input" placeholder="请输入内容"></el-input>
        </div></el-col>
        <el-col :span="4"><div class="grid-content bg-purple-light"></div></el-col>
        <el-col :span="4"><div class="grid-content bg-purple"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple-light"></div></el-col>
        <el-col :span="6"><div class="grid-content bg-purple"></div></el-col>
      </el-row>



    </el-tab-pane>
    <el-tab-pane label="待试验" name="second">待试验</el-tab-pane>
    <el-tab-pane label="待复核" name="third">待复核</el-tab-pane>
    <el-tab-pane label="待批准" name="fourth">待批准</el-tab-pane>
    <el-tab-pane label="待确认" name="fifth">待确认</el-tab-pane>
    <el-tab-pane label="已确认" name="sixth">已确认</el-tab-pane>

  </el-tabs>


</div>
</template>

<script>
export default {
  name: "testMange",
  data(){
    return {
      activeName: 'first',
      input: ''
    }
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    }
  }
}
</script>

<style scoped lang="less">
.el-row {
  margin-bottom: 20px;
  &:last-child {
    margin-bottom: 0;
  }
}
.el-col {
  border-radius: 4px;
}
.bg-purple-dark {
  background: #99a9bf;
}
.bg-purple {
  background: #d3dce6;
}
.bg-purple-light {
  background: #e5e9f2;
}
.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
.row-bg {
  padding: 10px 0;
  background-color: #f9fafc;
}
</style>
