<template>
  <el-radio-group v-model="tabIndex" style="margin-bottom: 30px">
    <el-radio-button label="file">file</el-radio-button>
    <el-radio-button label="protol">protol</el-radio-button>
    <el-radio-button label="code">代码分析</el-radio-button>
    <el-radio-button label="fault">故障分析</el-radio-button>
  </el-radio-group>

  <el-tabs tab-position="left" style="height: 200px" v-show="tabIndex === 'file'">
    <el-tab-pane label="文件拼接"></el-tab-pane>
    <el-tab-pane label="文件属性"></el-tab-pane>
    <el-tab-pane label="文件转换"></el-tab-pane>
  </el-tabs>
  <el-tabs tab-position="left" style="height: 400px" v-show="tabIndex === 'protol'">
    <el-tab-pane label="新CAN"></el-tab-pane>
    <el-tab-pane label="老CAN"></el-tab-pane>
    <el-tab-pane label="MB"></el-tab-pane>
    <el-tab-pane label="主从"></el-tab-pane>
    <el-tab-pane label="TCP-MB"></el-tab-pane>
    <el-tab-pane label="BIN"></el-tab-pane>
  </el-tabs>
</template>
<script>
export default {
  data() {
    return {
      tabIndex: 'file',
    }
  },
}
</script>

