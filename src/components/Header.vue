<template>
  <div>
    <el-row class="el-row" type="flex" align="middle" >
      <el-col class="el-col" :span="18">
        <div>
          <img style="float:left; height:30px; width:30px; margin-left: 20px; margin-right:20px; margin-top: 10px"
                src="../assets/GEE Logo.png" @click="homeClick"/>
          <el-menu
            style="float: left; height:60px"
            :default-active="activeIndex"
            class="el-menu-demo"
            mode="horizontal"
            @select="handleSelect"
          >
        <el-menu-item class="el-menu-item" index="1">Home</el-menu-item>
        <el-menu-item index="2">Consultants</el-menu-item>
        <el-submenu index="3">
          <template slot="title">Menu</template>
          <el-menu-item index="3-1">选项1</el-menu-item>
          <el-menu-item index="3-2">选项2</el-menu-item>
          <el-menu-item index="3-3">选项3</el-menu-item>
        </el-submenu>
          </el-menu>
        </div>
      </el-col>
      <el-col :span="6" align="middle">
        <el-row type="flex" align="middle" justify="end" style="margin-right:20px">
          <el-button type="primary" @click="loginClick">登录</el-button>
          <el-button @click="registerClick">注册</el-button>
        </el-row>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      activeIndex: '1',
      activeIndex2: '1'
    }
  },
  methods: {
    handleSelect (key, keyPath) {
      console.log(key, keyPath)
    },
    homeClick () {
      this.$router.push('')
    },
    loginClick () {
      this.$router.push('login')
    },
    registerClick () {
      this.$router.push('register')
    }
  }
}
</script>

<style scoped>
.el-menu {
  height: 10px;
  border-bottom: none;
}
</style>
