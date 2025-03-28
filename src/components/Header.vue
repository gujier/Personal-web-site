<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="header">
    <div class="nav-circle" @mouseenter="isHovered = true" @mouseleave="isHovered = false">
      <div class="circle"></div>
      <div class="nav-content" :class="{ active: isHovered }">
        <nav>
          <div class="nav-links">
            <RouterLink to="/">首页</RouterLink>
            <RouterLink to="/content1">内容1</RouterLink>
            <RouterLink to="/content2">内容2</RouterLink>
            <RouterLink to="/content3">内容3</RouterLink>
          </div>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isHovered: false
    }
  }
}
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
}

.nav-circle {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  height: 100px;
}


.nav-content {
  position: absolute;
  top: -150%; /* 初始位置在视图上方 */
  width: 100%;
  background: #2c3e50;
  transition: top 0.5s ease; /* 动画效果 */
  z-index: 1;
  padding-top: 60px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.nav-content.active {
  top: -50%; /* 最终位置在视图顶部 */
}

nav {
  max-width: 1200px;
  margin: 0 auto;
  padding: 1rem 2rem;
}

.nav-links {
  display: flex;
  justify-content: center;
  gap: 2rem;
}

.nav-links a {
  color: white;
  text-decoration: none;
  font-size: 1.1rem;
  padding: 0.5rem 1rem;
  border-radius: 5px;
  transition: all 0.3s ease;
}

.nav-links a:hover {
  color: #42b983;
  background: rgba(255, 255, 255, 0.1);
}

.router-link-active {
  color: #42b983 !important;
  font-weight: bold;
}
</style>
