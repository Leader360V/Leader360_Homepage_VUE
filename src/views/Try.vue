<template>
  <div class="try-demo-root">
    <header class="try-header">
      <div class="try-header-row">
        <div>
          <div class="try-title">
            <span class="gradient">Automatic Annotate Any 360 Video Pipeline</span>
          </div>
        </div>
        <div class="button-group">
          <div class="try-btn-gradient">
            <a href="" target="_blank" class="try-btn">Submit</a>
          </div>
          <div class="try-btn-gradient">
            <a href="" target="_blank" class="try-btn">Process</a>
          </div>
        </div>
      </div>
    </header>
    <div class="feature-grid">
      <div class="feature-label">
        <h3 class="about-card-sm-title">Raw Input</h3>
      </div>
      <div class="feature-label">
        <h3 class="about-card-sm-title">Annotation</h3>
      </div>
    </div>
    <main class="try-main">
      <div class="video-container">
        <div class="try-video-wrapper">
          <video
            class="try-video"
            src="/assets/feature1.mp4"
            autoplay
            loop
            muted
            playsinline
            controls
          ></video>
        </div>
        <div class="try-video-wrapper">
          <video
            class="try-video"
            src="/assets/feature1.mp4"
            autoplay
            loop
            muted
            playsinline
            controls
          ></video>
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
// 无需逻辑
</script>

<style scoped>
.try-demo-root {
  min-height: 100vh;
  background: #fff;
  color: #111;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.try-header {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 48px 0 24px 0;
  text-align: left;
}
.try-header-row {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 32px;
}
.try-title {
  font-size: 2.6rem;
  font-weight: 700;
  margin-bottom: 12px;
  letter-spacing: -1px;
}
.gradient {
  background: linear-gradient(90deg, #e05297 10%, #6c63ff 40%, #2ec4b6 70%, #ffe066 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
.try-btn-gradient {
  display: inline-block;
  padding: 2.5px;
  border-radius: 999px;
  background: linear-gradient(90deg, #e05297 10%, #6c63ff 40%, #2ec4b6 70%, #ffe066 100%);
}
.try-btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  background: #111;
  color: #fff;
  border-radius: 999px;
  padding: 12px 32px;
  font-size: 1.1rem;
  font-weight: 600;
  text-decoration: none;
  border: none;
  min-width: 120px;
  min-height: 44px;
  box-shadow: 0 2px 12px rgba(0,0,0,0.08);
  transition: background 0.2s, color 0.2s;
}
.try-btn:hover {
  background: #fff;
  color: #111;
}
.try-main {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: flex-start;
}
.video-container {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  width: 100vw;
  max-width: 1200px;
  margin: 32px auto;
  padding: 20px;
  background: #f8f8f8;
  border-radius: 16px;
  box-shadow: 0 4px 32px rgba(0,0,0,0.18);
}
.try-video-wrapper {
  width: 45%;
  border-radius: 16px;
  overflow: hidden;
  background: #000;
  box-shadow: 0 4px 32px rgba(0,0,0,0.18);
}
.try-video {
  width: 100%;
  height: auto;
  display: block;
  background: #000;
}
.feature-grid {
  display: flex;
  justify-content: space-between;
  width: 90vw;
  max-width: 1200px;
  margin: 0 auto;
  margin-top: 16px;
}
.feature-label {
  width: 50%;
  text-align: center;
}
.about-card-sm-title {
  font-size: 1.3rem;
  font-weight: 700;
  margin-bottom: 20px;
  color: #111;
}
.button-group {
  display: flex;
  gap: 8px;
}
@media (max-width: 900px) {
  .try-header {
    padding: 32px 0 16px 0;
  }
  .try-header-row {
    flex-direction: column;
    align-items: flex-start;
    gap: 18px;
  }
  .try-title {
    font-size: 2rem;
  }
  .video-container {
    flex-direction: column;
  }
  .try-video-wrapper {
    width: 100%;
    margin-bottom: 16px;
  }
}
</style>