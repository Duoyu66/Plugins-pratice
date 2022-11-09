<template>
  <el-tabs v-model="activeName" type="card" @tab-click="handleClick">
    <el-tab-pane label="试验修改记录" name="first">
      <el-row>
        <el-col :span="12" style="padding-right: 10px">
          <div class="grid-content bg-purple">

            <el-table
              fit=true
              height=300
              :header-cell-style="headClass"
              style="width: 100%">
              <el-table-column
                prop="date"
                label="申请时间">
              </el-table-column>
              <el-table-column
                prop="name"
                label="申请人">
              </el-table-column>
              <el-table-column
                prop="address"
                label="审批人">
              </el-table-column>
              <el-table-column
                prop="address"
                label="审批时间">
              </el-table-column>
            </el-table>

            <Pagination></Pagination>
          </div>
        </el-col>
        <el-col :span="12" style="padding-left: 10px">
          <div class="grid-content bg-purple-light"><div class="grid-content bg-purple">

            <el-table
              fit=true
              height=300
              :header-cell-style="headClass"
              style="width: 100%">
              <el-table-column
                prop="date"
                label="申请时间">
              </el-table-column>
              <el-table-column
                prop="name"
                label="申请人">
              </el-table-column>
              <el-table-column
                prop="address"
                label="审批人">
              </el-table-column>
              <el-table-column
                prop="address"
                label="审批时间">
              </el-table-column>
            </el-table>

            <Pagination></Pagination>
          </div></div>
        </el-col>
      </el-row>
    </el-tab-pane>
    <el-tab-pane label="试验任务" name="second">
      <el-row>
        <el-col :span="12">
          <div class="grid-content bg-purple">

            <el-table
              fit=true
              height=300
              :header-cell-style="headClass"
              style="width: 100%">
              <el-table-column
                prop="date"
                label="申请时间">
              </el-table-column>
              <el-table-column
                prop="name"
                label="申请人">
              </el-table-column>
              <el-table-column
                prop="address"
                label="审批人">
              </el-table-column>
              <el-table-column
                prop="address"
                label="审批时间">
              </el-table-column>
            </el-table>

            <Pagination></Pagination>
          </div>
        </el-col>
        <el-col :span="12">
          <div class="grid-content bg-purple-light">46546</div>
        </el-col>
      </el-row>
    </el-tab-pane>
  </el-tabs>
</template>

<script>
import Pagination from "@/components/Pagination";

export default {
  components: {Pagination},
  name: "index",
  data() {
    return {
      activeName: 'first'
    };
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    },
    headClass() {
      return 'text-align: center;background:#eef1f6;'
    },
  }
}
</script>

<style scoped>

</style>
