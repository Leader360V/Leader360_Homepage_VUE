<template>
  <section id="research" class="research">
    <div class="container research-flex">
      <div class="research-left">
        <h2>Why Collect Additional Videos by Ourselves?</h2>
        <p class="research-desc">
          Imbalance in existing datasets
        </p>
        <div class="research-highlights-box">
          <div class="research-highlights-title"><b>Highlights</b></div>
          <ul class="research-highlights-list">
            <li>More Scenario Diversity: overall sceanrios reach 1K.</li>
            <li>Multiple Shooting Way: </li>
            <li>More Balanced Distribution: </li>
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