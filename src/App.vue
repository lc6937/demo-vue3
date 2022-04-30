<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App" />

    <div class="content" new></div>

    jjjj
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
  },
};
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: red;

  width: 100%;
  margin-top: 200px;
  height: calc(100vh - 200px);

  .content {
    width: 200px;
    height: 200px;
  }
}
</style>
