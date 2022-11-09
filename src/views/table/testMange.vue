<template>
  <div>

    <el-tabs v-model="activeName" @tab-click="handleClick" style="margin-left: 20px">
      <el-tab-pane label="全部台账" name="first">

        <el-row>
          <el-col :span="4">
            <div class="grid-content bg-purple">
              <el-input v-model="input" placeholder="按委托编号搜索"></el-input>
            </div>
          </el-col>
          <el-col :span="4">
            <div class="grid-content bg-purple-light ge">
              <el-input v-model="input" placeholder="按报告编号搜索"></el-input>

            </div>
          </el-col>
          <el-col :span="4">
            <div class="grid-content bg-purple ge">
              <el-input v-model="input" placeholder="按批号搜索"></el-input>

            </div>
          </el-col>
          <el-col :span="10">
            <div class="grid-content bg-purple-light ge">
              <div class="block">
                <el-date-picker
                  v-model="value1"
                  type="daterange"
                  range-separator="至"
                  start-placeholder="开始日期"
                  end-placeholder="结束日期">
                </el-date-picker>
              </div>
            </div>

          </el-col>
          <el-col :span="2">
            <div class="grid-content bg-purple">
              <el-button type="primary" icon="el-icon-search" class="sou">搜索</el-button>
            </div>
          </el-col>
        </el-row>


      </el-tab-pane>
      <el-tab-pane label="待试验" name="second">待试验</el-tab-pane>
      <el-tab-pane label="待复核" name="third">待复核</el-tab-pane>
      <el-tab-pane label="待批准" name="fourth">待批准</el-tab-pane>
      <el-tab-pane label="待确认" name="fifth">待确认</el-tab-pane>
      <el-tab-pane label="已确认" name="sixth">已确认</el-tab-pane>

    </el-tabs>
<entrustTable></entrustTable>
<Pagination></Pagination>
    <Footer></Footer>
  </div>
</template>

<script>
import entrustTable from "@/views/table/entrustTable";
import Pagination from '@/components/Pagination';
import Footer from "@/views/table/Footer";
export default {
  name: "testMange",
  components: {entrustTable,Pagination,Footer},

  data() {
    return {
      activeName: 'first',
      input: '',
      value1: '',
      value2: ''
    }
  }
}
</script>

<style scoped lang="less">
.sou{
  padding-left: -600px;
}
.ge {
  padding-left: 20px;
}

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
  background: #fff;
}

.bg-purple {
  background: #d3dce6;
}

.bg-purple-light {
  background: #fff;
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
