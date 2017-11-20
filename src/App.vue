<template>
  <div id="app">
    <div class="btn" @click="alert">alert</div>
    <div class="btn" @click="confirm">confirm</div>
    <div class="btn" @click="toast">toast</div>
    <div class="btn" @click="loading">loading</div>
    <div class="btn" @click="success">success</div>
    <div class="btn" @click="error">error</div>
    <div class="btn" @click="createAip">createAip</div>
  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld'

  export default {
    name: 'app',
    methods: {
      alert () {
        this.Dialog().setText('哈哈哈').setType('alert').show()
      },
      confirm () {
        this.Dialog().setText('哈哈哈').setType('confirm').show()
      },
      toast () {
        this.Toast().setText('哈哈哈').show()
      },
      loading () {
        this.Loading().setText('哈哈哈').show()
      },
      success () {
        this.Loading().setType('success').setText('哈哈哈').show()
      },
      error () {
        this.Loading().setType('error').setText('哈哈哈').show()
      },
      createAip () {
        this.$createAip(HelloWorld).show()
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
    margin-top: 60px;
  }
</style>
