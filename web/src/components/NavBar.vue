<script setup>
import { useRoute } from 'vue-router'
const route = useRoute()
const handleClick = () => {
  window.location = 'http://localhost:5174'
}
</script>
<template>
  <div class="navbar">
    <el-menu :default-active="route.fullPath" class="el-menu-demo" mode="horizontal" :router="true">
      <el-menu-item index="/">首页</el-menu-item>
      <el-menu-item index="/news">新闻中心</el-menu-item>
      <el-menu-item index="/product">产品中心</el-menu-item>
      <el-menu-item @click="handleClick">登录</el-menu-item>
    </el-menu>
    <div class="right">企业门户官网</div>
  </div>
</template>
<style scoped lang="scss">
.navbar {
  position: sticky;
  top: 0;
  z-index: 1000;
}
.right {
  position: fixed;
  top: 0;
  right: 20px;
  widows: 100px;
  height: 60px;
  line-height: 60px;
}
</style>
