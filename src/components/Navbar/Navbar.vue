<template>
    <div class="nav">
      <!-- Logo -->
      <img src="../../assets/logo.png" />

      <!-- 搜索框 -->
      <el-input placeholder="请输入要搜索的内容" v-model="search" class="input-with-select" clearable>
        <el-select v-model="select" slot="prepend" placeholder="全部">
          <el-option label="用户" value="1"></el-option>
          <el-option label="话题" value="2"></el-option>
          <el-option label="分类" value="3"></el-option>
        </el-select>
        <i slot="suffix" class="el-input__icon el-icon-search"></i>
      </el-input>

      <!-- 导航 -->
      <ul class="menu">
        <li><a href="#"><i class="el-icon-s-home"></i> 首页</a></li>
        <li><a href="#"><i class="el-icon-magic-stick"></i> 发现</a></li>
        <li><a href="#"><i class="el-icon-share"></i> 话题</a></li>
        <li><a href="#"><i class="el-icon-user-solid"></i> 个人中心</a></li>
      </ul>

      <!-- 更换背景 -->
      <div class="bg">
        <BgSwitch></BgSwitch>
      </div>
    </div>
</template>

<script>
  import BgSwitch from '@/components/Navbar/BgSwitch'
  export default {
    name: 'Navbar',
    components: {BgSwitch},
    data () {
      return {
        search: '',
        select: ''
      }
    }
  }
</script>

<style scoped>
  ul,li{

  }
  li{
    list-style: none;
  }
  a{
    text-decoration: none;
  }
  .nav{
    border: 1px solid black;
    width: 100%;
  }
  img{
    width: 15%;
    vertical-align: middle;
  }
  .el-input{
    width: 30%;
    vertical-align: middle;
  }
  .el-select{
    /*border: 1px saddlebrown solid;*/
    width: 75rem;
    padding-left: 0;
  }

  /* /deep/ 深度样式，会覆盖elementUI的默认样式 */
  /deep/ .input-with-select{
    font-size: 12rem;
  }
  /deep/ .el-input__inner{
    height: 30rem;
    padding-left: 10rem;
    padding-right: 20rem;
  }
  /deep/ .el-input__icon{
    line-height: 30rem;
  }

  .menu{
    width: 40%;
    height: 45rem;
    padding: 0;
    font-size: 18rem;
    line-height: 45rem;
    margin: 0 0 0 40rem;
    display: inline-block;
    vertical-align: middle;
    /*border: 1px solid red;*/
  }
  .menu li{
    float: left;
    width: 21%;
  }
  .menu li:last-of-type{
    width: 36%;
  }
  .bg{
    width: 8%;
    vertical-align: middle;
    display: inline-block;
  }
</style>
