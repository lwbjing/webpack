<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>{{ input1 }}</h1>
    <div style=" width: 200px; margin: 0 auto 10px;">
      <el-input placeholder="请输入标题" icon="edit" v-model="input1" :on-icon-click="handleIconClick"></el-input>
    </div>
    <el-button @click.native="startHacking">Click Me!</el-button>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      input1: '这个是标题啊'
    }
  },
  methods: {
    startHacking () {
      this.$notify({
        title: 'It Works',
        message: 'We have laid the groundwork for you. Now it\'s your time to build something epic!',
        duration: 6000
      })
    },
    handleIconClick (ev) {
      console.log(ev);
    }
  }
}
</script>

<style>
body {
  font-family: Helvetica, sans-serif;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
