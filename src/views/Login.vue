<template>
  <div class = "login_container">
    <div class = "login_box">
      <div class = "avatar_box">
        <img src="../assets/avatar.gif">
      </div>
      <el-form :model="loginForm" :rules="loginRules" ref="loginForm" label-width="70px" class="login_Form">
        <el-form-item label="公司ID:" prop="companyId">
          <el-input v-model="loginForm.companyId" prefix-icon="el-icon-suitcase"></el-input>
        </el-form-item>
        <el-form-item label="账    号:" prop="account">
          <el-input v-model="loginForm.account" prefix-icon="el-icon-user-solid"></el-input>
        </el-form-item>
        <el-form-item label="密    码:" prop="password">
          <el-input type="password" v-model="loginForm.password" prefix-icon="el-icon-lock"></el-input>
        </el-form-item>
        <el-form-item class = "login_btn">
          <el-button type="primary" @click="submitForm('loginForm')">登  录</el-button>
          <el-button @click="resetForm('loginForm')">重   置</el-button>
        </el-form-item>
      </el-form>
    </div>
  </div>
</template>

<script>
export default {
    name: "Login",
    data() {
      return {
        loginForm: {
          companyId: '',
          account: '',
          password: ''
        },
        loginRules: {
          companyId: [
            { required: true, message: '请输入公司ID', trigger: 'blur' },
            { min: 7, max: 7, message: '长度为7个字符的公司ID', trigger: 'blur' }
          ],
          account: [
            { required: true, message: '请输入用户账号', trigger: 'blur' },
            { min: 6, max: 50, message: '长度大于5个字符的用户账号', trigger: 'blur' }
          ],
          password: [
            { required: true, message: '请输入密码', trigger: 'blur' },
            { min: 6, max: 50, message: '长度大于5个字符的密码', trigger: 'blur' }
          ]
        }
      };
  },
  methods: {
    submitForm(formName) {
      this.$refs[formName].validate((valid) => {
        if (valid) {
          this.$router.push("/main")
        } else {
          console.log('error submit!!');
          return false;
        }
      });
    },
    resetForm(formName) {
      this.$refs[formName].resetFields();
    }
  }
}
</script>

<style scoped>
  .login_btn{
    display: flex;
    justify-content: flex-end;
  }
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
  .login_Form{
    position: absolute;
    bottom: 0px;
    width: 95%;
    padding: 0px;
  }

</style>