<template>
  <section id="resources" class="resources">
    <div class="container">
      <h2 class="resources-title">Explore Additional Resources</h2>
      <div class="resources-grid">
        <a href="#" class="resources-card">
          <span>Back to Top</span>
          <span class="resources-arrow">&#8599;</span>
        </a>
        <a href="#" class="resources-card">
          <span>Read the Research Paper</span>
          <span class="resources-arrow">&#8599;</span>
        </a>
        <a href="https://huggingface.co/datasets/Leader360V/Leader360V" class="resources-card">
          <span>Download the Dataset</span>
          <span class="resources-arrow">&#8599;</span>
        </a>
        <a href="https://leader360v.github.io/Leader360V_HomePage" class="resources-card">
          <span>Explore More</span>
          <span class="resources-arrow">&#8599;</span>
        </a>
        <!-- <a href="#" class="resources-card">
          <span>Download the model</span>
          <span class="resources-arrow">&#8599;</span>
        </a> -->
      </div>
    </div>
  </section>
</template>

<script setup>
// 暂无逻辑
</script>

<style scoped>
.resources {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 0;
}
.resources-title {
  font-size: 2em;
  margin: 0 0 24px 0;
}
.resources-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 24px;
}
.resources-card {
  background: #f9f9f9;
  border-radius: 12px;
  padding: 24px;
  text-decoration: none;
  color: #333;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: background 0.3s;
}
.resources-card:hover {
  background: #e9e9e9;
}
.resources-arrow {
  font-size: 1.2em;
}
.resources-bg {
  /* 移除背景色 */
}
</style> 