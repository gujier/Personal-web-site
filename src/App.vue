<script setup>
import { RouterLink, RouterView } from 'vue-router'
import headernav from './components/Header.vue'
</script>

<template>
  <div class="app-container">
    <headernav/>
    <RouterView />
  </div>
</template>

<style>
.app-container {
  padding-top: 100px;
  min-height: 100vh;
  background-image: url('/src/assets/img/00004-1828958346.png');
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
  background-repeat: no-repeat;
  width: 100vw; /* 修改为视口宽度 */
  margin: 0; /* 新增 */
  overflow: hidden; /* 新增 */
}
</style>
