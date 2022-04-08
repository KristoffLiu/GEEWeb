<template>
  <el-header>
    <el-row class="el-row" type="flex" align="middle">
      <el-col class="el-col" :span="18">
        <div style="height: 60px">
          <img
            style="
              float: left;
              height: 30px;
              width: 30px;
              margin-left: 20px;
              margin-right: 20px;
              margin-top: 15px;
              cursor: pointer;
            "
            src="../assets/GEE Logo.png"
            @click="homeClick"
          />
        </div>
      </el-col>
      <el-col :span="6" align="middle">
        <el-row
          type="flex"
          align="middle"
          justify="end"
          style="margin-right: 20px"
        >
          <el-button type="primary" @click="loginClick">登录</el-button>
          <el-button @click="registerClick">注册</el-button>
        </el-row>
      </el-col>
    </el-row>
  </el-header>
</template>
<script>

export default({
  methods: {
    homeClick () {
      this.$router.push('/')
    },
    loginClick () {
      this.$router.push('login')
    },
    registerClick () {
      this.$router.push('register')
    },
    next () {
      if (this.active++ > 3) this.active = 0
    }
  }
})
</script>
