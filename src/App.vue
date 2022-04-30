<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <div class="left">菜单</div>

    <div class="right">
      <div class="header">头部</div>
      <div class="content">内容</div>
      <div class="footer">尾部</div>
    </div>
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
/*菜单样式定义*/
@menu-bc: #aaa;
@menu-width: 100px;

/*头部样式定义*/
@header-bc: #ccc;
@header-height: 64px;

/*尾部样式定义*/
@footer-height: 32px;
@footer-bc: #ccc;

/*内容样式定义*/
@content-bc: #bbb;
@content-height: @header-height + @footer-height;

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  color: #2c3e50;
  background-color: red;
  display: flex;

  width: 100%;
  height: calc(100vh);

  .left {
    max-width: @menu-width;
    min-width: @menu-width;
    display: flex;
    height: calc(100vh);
    overflow: auto;
    background-color: @menu-bc;
  }

  .right {
    width: 100%;
    height: calc(100vh);
    overflow: auto;
    background-color: @content-bc;

    .header {
      width: 100%;
      height: @header-height;
      color: blue;
      background-color: @header-bc;
    }
    .content {
      width: 100%;
      height: calc(100vh - @content-height);
      overflow: auto;
      background-color: @content-bc;
      margin-top: @header-height;
    }
    .footer {
      width: 100%;
      height: @footer-height;
      color: blue;
      text-algin: center;
      background-color: @footer-bc;
    }
  }
}
</style>
