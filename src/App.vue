<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <div class="left">菜单</div>

    <div class="content">测试</div>
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
@menu-bc: #aaa;
@content-bc: #bbb;
@header-bc: #ccc;

@menu-width: 100px;
@header-height: 64px;

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  background-color: red;
  display: flex;

  width: 100%;
  height: calc(100vh);

  .content {
    width: 100%;
    height: calc(100vh - @header-height);
    overflow: auto;
    background-color: @content-bc;
    margin-top: @header-height;
  }

  .left {
    max-width: @menu-width;
    min-width: @menu-width;
    display: flex;
    height: calc(100vh);
    overflow: auto;
    background-color: @menu-bc;
  }
}
</style>
