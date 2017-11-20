<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div ref="scsc"></div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
export default {
  name: 'app',
  created(){
    this.Dialog().setText('哈哈哈').setType('alert').show()
  },
  mounted(){
    this.createAip(HelloWorld).setRoot(this.$refs['scsc']).show()
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
  margin-top: 60px;
}
</style>
