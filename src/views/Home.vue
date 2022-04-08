<template>
  <div>
    <el-row class="mainpagestyle" type="flex" justify="center" align="middle">
      <div>
        <img style="float:left; max-height:200px" src="../assets/Consultant.png"/>
        <img style="float:left; max-height:200px" src="../assets/Clinet.png"/>
      </div>
    </el-row>

    <el-row>
      <h2 id="aboutUs" class="text-center">About us</h2>
      <p class="fontt">Global Episteme Exousia aims to be an online platform that matches academic and industrial experts in the fields of cutting edge technologies such as artificial intelligence, aerospace and aeronautics, biomedicine and genetic engineering, with corporations, media institutions and students with educational needs for decision making. We hope to bridge the information gap between academia and industries across the Asia-pacific and make technological innovations more ethical and accountable. </p>
    </el-row>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
  }
}
</script>

<style scoped>
.mainpagestyle {
  background:url("../assets/banner.gif");
  height:400px
}
.fontt {
  font-family: "Helvetica Neue",Helvetica,"PingFang SC","Hiragino Sans GB","Microsoft YaHei","微软雅黑",Arial,sans-serif;
  line-height: 1.5;
}
</style>
