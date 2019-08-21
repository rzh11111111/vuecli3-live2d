<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <hello-world></hello-world>
    <live2d></live2d>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import live2d from './components/live2d.vue'
export default {
  name: 'app',
  components: {
    HelloWorld,live2d
  },
  mounted(){
    
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
