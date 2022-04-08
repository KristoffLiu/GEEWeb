<template>
  <div>
    <el-main>
      <el-row type="flex" justify="start">
        <el-col :span="6" style="margin-top:10px; margin-bottom: 40px">
          <h1>注册</h1>
        </el-col>
      </el-row>
      <el-row>
        <el-col>
          <el-steps style="margin-left:10px; margin-right:10px" :active="active" finish-status="success" align-center>
            <el-step title="账号及密码"></el-step>
            <el-step title="基本信息"></el-step>
            <el-step title="检查"></el-step>
            <el-step title="注册完成"></el-step>
          </el-steps>
        </el-col>
      </el-row>
      <el-row style="margin-top: 40px; margin-bottom: 20px">
        <el-col :span="10" offset="2">
          <el-form label-width="80px">
            <el-form-item label="邮箱地址" required>
              <el-input></el-input>
            </el-form-item>
            <el-form-item label="密码" required>
              <el-input></el-input>
            </el-form-item>
            <el-form-item label="重复密码" required>
              <el-input></el-input>
            </el-form-item>
            <el-form-item label="验证码" required>
              <el-input style="float:left; width:200px"></el-input>
              <div class="captcha_code">
                <img ref="code" src="../assets/verifyCode.png">
              </div>
            </el-form-item>
          </el-form>
        </el-col>
      </el-row>
      <!-- <el-row style="margin-top: 10px; margin-bottom: 20px">
        <el-row style="margin-top: 20px">
          <el-col span="10" offset="2">
            <div style="text-align:left; margin-left: 17px; height:30px;">邮箱地址</div>
            <el-input v-model="input" placeholder="请输入邮箱"></el-input>
          </el-col>
        </el-row>
        <el-row style="margin-top: 20px">
          <el-col span="10" offset="2">
            <div style="text-align:left; margin-left: 17px; height:30px;">密码</div>
            <el-input v-model="input" placeholder="请输入密码"></el-input>
          </el-col>
        </el-row>
        <el-row style="margin-top: 20px">
          <el-col span="10" offset="2">
            <div style="text-align:left; margin-left: 17px; height:30px;">重复输入密码</div>
            <el-input v-model="input" placeholder="请输入密码"></el-input>
          </el-col>
        </el-row>
        <el-row style="margin-top: 20px">
          <el-col span="10" offset="2">
            <div style="text-align:left; margin-left: 17px; height:30px;">验证码</div>
            <el-input v-model="input" placeholder="请输入验证码"></el-input>
          </el-col>
        </el-row>
      </el-row> -->
      <el-row style="margin-top: 20px; margin-bottom:240px">
        <el-col :span="6">
          <el-button style="margin-top: 12px; margin-left:10px" @click="next"
                     type="primary">下一步</el-button>
        </el-col>
      </el-row>
    </el-main>
  </div>
</template>
<script>
export default {
  data () {
    return {
      active: 0
    }
  }
}
</script>

<style scoped>
.login-container {
  width: 100%;
  height: 100%;
}
.login-page {
  -webkit-border-radius: 5px;
  border-radius: 5px;
  margin: 180px auto;
  width: 1000px;
  padding: 35px 35px 15px;
  background: #fff;
  border: 1px solid #eaeaea;
  box-shadow: 0 0 25px #cac6c6;
}
label.el-checkbox.rememberme {
  margin: 0px 0px 15px;
  text-align: left;
}
</style>
