<template>
  <section id="research" class="research">
    <div class="container research-flex">
      <div class="research-left">
        <h2>State-of-the-art<br>performance for object segmentation</h2>
        <p class="research-desc">
          SAM 2 outperforms the best models in the field for object segmentation in videos and images.
        </p>
        <div class="research-highlights-box">
          <div class="research-highlights-title"><b>Highlights</b></div>
          <ul class="research-highlights-list">
            <li>SAM 2 improves on SAM for segmentation in images</li>
            <li>SAM 2 outperforms existing video object segmentation models, especially for tracking parts</li>
            <li>SAM 2 requires less interaction time than existing interactive video segmentation methods</li>
          </ul>
        </div>
      </div>
      <div class="research-right">
        <video class="research-video" src="/assets/demo.mp4" autoplay loop muted playsinline controls></video>
      </div>
    </div>
  </section>
</template>

<script setup>
// 暂无逻辑
</script>

<style scoped>
.research {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 0;
}
.research-flex {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.research-left {
  flex: 1.2;
  padding-right: 40px;
}
.research-right {
  flex: 1;
  display: flex;
  justify-content: center;
}
.research-video {
  width: 100%;
  max-width: 400px;
  border-radius: 18px;
  box-shadow: 0 4px 32px rgba(0,0,0,0.12);
}
.research-desc {
  font-size: 1.2em;
  color: #555;
  margin-bottom: 24px;
}
.research-highlights-box {
  background: #f9f9f9;
  border-radius: 12px;
  padding: 16px;
  margin-top: 24px;
  text-align: left;
}
.research-highlights-title {
  font-size: 1.2em;
  margin-bottom: 8px;
}
.research-highlights-list {
  list-style-type: disc;
  padding-left: 20px;
}
</style> 