<script setup>
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
    <div>
    <h1>子应用👇</h1>
    <!-- name：应用名称, url：应用地址 -->
    <micro-app iframe name='my-app' url='http://localhost:5173/'></micro-app>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
