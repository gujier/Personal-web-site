<template>
  <div class="content1-view">
    <h1>大学经历</h1>
    <div class="experience-section">
      <h2>学习经历</h2>
      <p>这里可以填写大学期间的学习经历和收获。</p>
    </div>
    <div class="experience-section">
      <h2>项目经历</h2>
      <p>这里可以填写参与的项目和成果。</p>
    </div>
    <div class="experience-section">
      <h2>校园活动</h2>
      <p>这里可以填写参与的社团和活动经历。</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Content1View'
}
</script>

<style scoped>
.content1-view {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
  color: white;
}

.experience-section {
  margin-bottom: 2rem;
  padding: 1rem;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 8px;
}

experience-section h2 {
  color: #42b983;
  margin-bottom: 1rem;
}
</style>