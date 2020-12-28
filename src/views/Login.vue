<template>
  <div class = "login_container">
    <div class = "login_box">
      <div class = "avatar_box">
        <img src="../assets/avatar.gif">

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Login"
}
</script>

<style scoped>
  .login_container{
    height: 100%;
    background-color: #2c3e50;
  }
  .login_box{
    width: 450px;
    height: 380px;
    background-color: #FFFFFF;
    border-radius: 3px;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
  .avatar_box{
    width: 130px;
    height: 130px;
    border: 1px solid #EEEEEE;
    border-radius: 50%;
    padding: 2px;
    box-shadow: 0 2px 12px 0 rgba(0, 0, 0, 0.1);
    margin: -65px auto;
    background-color: #FFFFFF;


  }
  img{
    width: 100%;
    height: 100%;
    border-radius: 50%;
  }
</style>