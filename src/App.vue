<template>
  <el-container id="app">
    <el-Header>
      <component :is="currentHeader"/>
    </el-Header>
    <el-main>
      <router-view/>
    </el-main>
    <el-footer>
      <Footer/>
    </el-footer>
  </el-container>
</template>

<script>
import Header from './components/Header.vue'
import LORHeader from './components/LORHeader.vue'
import Footer from './components/Footer.vue'
export default {
  name: 'App',
  components: {
    Header,
    LORHeader,
    Footer
  },
  data () {
    return {
      currentHeader: 'Header'
    }
  },
  watch: {
    '$route': {
      handler (route) {
        if (route.name === 'Login' || route.name === 'Register') {
          this.currentHeader = 'LORHeader'
        } else {
          this.currentHeader = 'Header'
        }
      }
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
.el-container{
  height: 100%;
}
</style>
