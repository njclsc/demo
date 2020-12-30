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
        <el-aside width="200px">Aside</el-aside>
        <el-main>Main</el-main>
      </el-container>
    </el-container>
</template>

<script>
export default {
name: "Main"
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
    color: #333;
    align-items: center;
    font-size: 20px;
    .left_box {
      display: flex;
      align-items: center;
    }
  }

  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
    line-height: 200px;
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