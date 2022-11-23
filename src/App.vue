<template>
  <div id="app">
    <h1>test</h1>
    <p>{{ a }}</p>
    <!-- 根路由出口 -->
    <router-view/>
    <p class="text">hello world</p>
    <el-row>
      <el-button>默认按钮</el-button>
      <el-button type="primary">主要按钮</el-button>
      <el-button type="success">成功按钮</el-button>
      <el-button type="info">信息按钮</el-button>
      <el-button type="warning">警告按钮</el-button>
      <el-button type="danger">危险按钮</el-button>
    </el-row>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'

@Component // 类的修饰器
// 装饰器是ES草案中的一个新特性，不建议在生产环境使用，可能有调整
export default class App extends Vue {
  a = 1
  b = 2
  c = {
    a: 1,
    b: 2
  }
}
</script>
<style lang="scss" scoped>
// @import "~@/styles/variables.scss";

.text {
  color: $success-color;
}
</style>
