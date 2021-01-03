<template>
    <el-container class = "main_container">
      <el-header>
        <div class = "left_box">
          <img src="../assets/avatar.gif">
          <span>皮油一火系统</span>
        </div>
        <div class = "right_box">

          <el-dropdown>
            <img src="../assets/avatar.gif">
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item icon = "">退出登录</el-dropdown-item>
              <el-dropdown-item icon = "">狮子头</el-dropdown-item>
              <el-dropdown-item icon = "">螺蛳粉</el-dropdown-item>
              <el-dropdown-item icon = "">双皮奶</el-dropdown-item>
              <el-dropdown-item icon = "">蚵仔煎</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </div>
      </el-header>
      <el-container>
        <el-aside :width="isCollapse?'60px':'200px'">
          <!-- 展开收起-->
          <div class = "toggle_box" @click="toggleCollapse">|||</div>
          <el-menu
            default-active="2"
            class="el-menu-vertical-demo"
            @open="handleOpen"
            @close="handleClose"
            background-color="#2c3e50"
            text-color="#fff"
            active-text-color="#ffd04b"
            :collapse="isCollapse"
            :collapse-transition="false"
            :unique-opened="true">
            <el-submenu index = "1">
              <template slot = "title">
                <i class="el-icon-location"></i>
                <span>定位区域</span>
              </template>
              <el-menu-item index = "1-1">
                <i class="el-icon-location"></i>
                <span slot = "title">定位区域一</span>
              </el-menu-item>
            </el-submenu>
            <el-submenu index = "2">
              <template slot = "title">
                <i class="el-icon-location"></i>
                <span>定位区域</span>
              </template>
              <el-menu-item index = "2-1">
                <i class="el-icon-location"></i>
                <span slot = "title">定位区域一</span>
              </el-menu-item>
            </el-submenu>
          </el-menu>
        </el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
</template>

<script>
export default {
  name: "Main",
  data(){
    return{
      isCollapse: false
    }
  },
  methods:{
    toggleCollapse(){
      this.isCollapse = !this.isCollapse;
    }
  }
}
</script>

<style lang="less" scoped>
  .main_container{
    height: 100%;
  }
  .el-header{
    background-color: #2c3e50;
    display: flex;
    justify-content: space-between;
    padding-left: 0;
    color: #ffffff;
    align-items: center;
    font-size: 20px;
    .left_box {
      display: flex;
      align-items: center;
      img{
        width: 60px;
        height: 60px;
        border-radius: 50px;
      }
      span{
        margin-left: 15px;
      }
    }
    .right_box {
      .el-dropdown > img{
        width: 60px;
        height: 60px;
        border-radius: 50px;
        background-color: #05020f;
      }
    }
  }
 
  .el-aside {
    background-color: #2c3e50;
    color: #333;
      .el-menu{
        border-right: none;
      }
     .toggle_box{
       background-color: #2c3e50;
       font-size: 15px;
       font-weight: bold;
       line-height: 25px;
       color: #ffffFF;
       letter-spacing: 0.5em;
       text-align: center;
       cursor: pointer;
    }
  }

  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
  }
  .el-dropdown-link {
    cursor: pointer;
    color: #409EFF;
  }
  .el-icon-arrow-down {
    font-size: 12px;
  }
  .demonstration {
    display: block;
    color: #8492a6;
    font-size: 14px;
    margin-bottom: 20px;
  }
</style>