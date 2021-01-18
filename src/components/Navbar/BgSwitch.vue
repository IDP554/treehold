<template>
  <!-- 背景图切换 -->
  <el-popover
    placement="bottom"
    title="更换背景"
    width="200"
    trigger="manual"
    v-model="visible">
    <el-button slot="reference" @click="visible = !visible">
      <img src="../../../static/images/nav/bgbtn.png" />
    </el-button>
  </el-popover>
</template>

<script>
export default {
  name: 'BgSwitch',
  data() {
    return {
      visible: false
    }
  }
}
</script>

<style scoped>
  .el-button{
    padding: 0;
    background-color: transparent;
    border: 0;
  }
  img{
    width: 100%;
  }
</style>
