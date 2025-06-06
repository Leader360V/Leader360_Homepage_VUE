<template>
  <section id="open-innovation" class="open-innovation-section open-innovation-bg">
    <!-- <div class="container open-innovation-flex"> -->
    <div class="container">
      <div class="open-innovation-left">
        <!-- <div class="open-innovation-label">Access our research</div> -->
        <h2 class="open-innovation-title">Flexibility of Our Pipeline</h2>
        <p class="open-innovation-desc">
          Our annotation pipeline allows users to freely customize components, supporting interchangeable choices of 2D segmentors, LLMs, and downstream prompt strategies.
        </p>
        <!-- <a class="open-innovation-link" href="#" target="_blank">
          <span class="arrow">&#8599;</span>
          <span>Download the model</span>
        </a> -->
        <div class="open-innovation-highlights-box">
          <div class="open-innovation-highlights-title"><b>Highlights</b></div>
          <ul class="open-innovation-highlights-list">
            <li>Offering configurable support for both entity-level and panoptic-level models for 2D segmentation backbones. </li>
            <li>Supporting flexible integration of LLMs for semantic label verification, which can be customized via task-specific text prompts. </li>
            <li>Enabling multi-task annotation with minimal human intervention, including large-scale 2D video datasets and related tasks. </li>
          </ul>
        </div>
      </div>
      <!-- <div class="open-innovation-right">
        <video class="open-innovation-video" src="/assets/feature3.mp4" autoplay loop muted playsinline controls></video>
      </div> -->
    </div>
  </section>
</template>

<script setup>
// 暂无逻辑
</script>

<style scoped>
.open-innovation-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 0;
}
.open-innovation-flex {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.open-innovation-left {
  flex: 1.2;
  padding-right: 40px;
}
.open-innovation-right {
  flex: 1;
  display: flex;
  justify-content: center;
}
.open-innovation-video {
  width: 100%;
  max-width: 400px;
  border-radius: 18px;
  box-shadow: 0 4px 32px rgba(0,0,0,0.12);
}
.open-innovation-label {
  font-size: 1.2em;
  color: #42b883;
  margin-bottom: 8px;
}
.open-innovation-title {
  font-size: 2em;
  margin: 0 0 16px 0;
}
.open-innovation-desc {
  font-size: 1.2em;
  color: #555;
  margin-bottom: 16px;
}
.open-innovation-link {
  display: inline-block;
  margin-top: 18px;
  color: #42b883;
  font-weight: bold;
  text-decoration: underline;
}
.open-innovation-highlights-box {
  background: #fff;
  border-radius: 12px;
  padding: 16px;
  margin-top: 24px;
  text-align: left;
}
.open-innovation-highlights-title {
  font-size: 1.2em;
  margin-bottom: 8px;
}
.open-innovation-highlights-list {
  list-style-type: disc;
  padding-left: 20px;
}
.open-innovation-bg {
  background: #f7f8fa;
}
</style> 