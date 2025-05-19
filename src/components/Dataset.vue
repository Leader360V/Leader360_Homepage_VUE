<template>
  <section id="dataset" class="dataset-section">
    <div class="container dataset-flex">
      <div class="dataset-left">
        <video class="dataset-video" src="/assets/feature4.mp4" autoplay loop muted playsinline controls></video>
      </div>
      <div class="dataset-right">
        <div class="dataset-label">The Segment Anything Video Dataset</div>
        <h2 class="dataset-title">A large and diverse video segmentation dataset</h2>
        <p class="dataset-desc">
          SAM 2 was trained on a large and diverse set of videos and masklets (object masks over time), created by applying SAM 2 interactively in a model in the loop data-engine. The training data includes the SA-V dataset, which we are open sourcing.
        </p>
        <p class="dataset-desc">
          Please email <a href="mailto:support@segment-anything.com" class="dataset-mail">support@segment-anything.com</a> with any issues or questions regarding the SA-V dataset.
        </p>
        <a class="dataset-link" href="#" target="_blank">
          <span class="arrow">&#8594;</span>
          <span>Explore the dataset</span>
        </a>
        <div class="dataset-highlights-box">
          <div class="dataset-highlights-title"><b>Highlights</b></div>
          <ul class="dataset-highlights-list">
            <li>~600K+ masklets collected on ~51K videos</li>
            <li>Geographically diverse, real world scenarios collected across 47 countries</li>
            <li>Annotations include whole objects, parts, and challenging occlusions</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// 暂无逻辑
</script>

<style scoped>
.dataset-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 0;
}
.dataset-flex {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.dataset-left {
  flex: 1;
  display: flex;
  justify-content: center;
}
.dataset-right {
  flex: 1.2;
  padding-left: 40px;
}
.dataset-video {
  width: 100%;
  max-width: 400px;
  border-radius: 18px;
  box-shadow: 0 4px 32px rgba(0,0,0,0.12);
}
.dataset-label {
  font-size: 1.2em;
  color: #42b883;
  margin-bottom: 8px;
}
.dataset-title {
  font-size: 2em;
  margin: 0 0 16px 0;
}
.dataset-desc {
  font-size: 1.2em;
  color: #555;
  margin-bottom: 16px;
}
.dataset-mail {
  color: #42b883;
  text-decoration: underline;
}
.dataset-link {
  display: inline-block;
  margin-top: 18px;
  color: #42b883;
  font-weight: bold;
  text-decoration: underline;
}
.dataset-highlights-box {
  background: #f9f9f9;
  border-radius: 12px;
  padding: 16px;
  margin-top: 24px;
  text-align: left;
}
.dataset-highlights-title {
  font-size: 1.2em;
  margin-bottom: 8px;
}
.dataset-highlights-list {
  list-style-type: disc;
  padding-left: 20px;
}
</style> 