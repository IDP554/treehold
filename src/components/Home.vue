<template>
  <el-row>
    <el-col :xs="1" :sm="2" :md="3" :lg="4" :xl="5"><div class="grid-content bg-purple"></div></el-col>
    <el-col :xs="22" :sm="20" :md="18" :lg="16" :xl="14"><div class="grid-content bg-purple-light">
      <Navbar></Navbar>

    </div></el-col>
    <el-col :xs="1" :sm="2" :md="3" :lg="4" :xl="5"><div class="grid-content bg-purple"></div></el-col>
  </el-row>
</template>

<script>
import Navbar from '@/components/Navbar'
export default {
  name: 'Home',
  components: {Navbar}
}
</script>

<style scoped>
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    min-height: 36px;
    border: 1px solid red;
  }
</style>
