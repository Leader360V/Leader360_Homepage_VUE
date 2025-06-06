<template>
  <section class="hero-main">
    <div class="hero-content">
      <div class="hero-main-label">Anonymous submission to NeurIPS2025</div>
      <h1 class="hero-main-title"> A Large-scale, Real-world 360 Video Dataset for Multi-task Learning in Diverse Environments</h1>
      <p class="hero-main-desc">
        Leader360V is the first large-scale (10K+), labeled real-world 360 video datasets for instance segmentation and tracking. Our datasets enjoy high scene diversity, ranging from indoor and urban settings to natural and dynamic outdoor scenes.
      </p>
      <div class="hero-main-btns">
        <!-- <router-link to="/try" class="hero-main-btn primary">Try the demo</router-link> -->
        <a href="https://huggingface.co/datasets/Leader360V/Leader360V" class="hero-main-btn primary">Try the Dataset</a>
        <a href="https://leader360v.github.io/Leader360V_HomePage/Dataset.html" class="hero-main-btn primary">Know More</a>
      </div>
    </div>
    <div class="open-innovation-right">
      <img class="open-innovation-video" src="/assets/img/Teaser_Figure_1_00.png">
    </div>
    <!-- <div class="hero-video">
      <transition name="fade" mode="out-in">
        <video
          v-if="currentVideo"
          :key="currentVideo"
          :src="currentVideo"
          autoplay
          loop
          muted
          playsinline
          class="main-video"
        ></video>
      </transition>
      <div class="video-controls">
        <button
          v-for="(video, idx) in videos"
          :key="video"
          :class="{ active: idx === currentIndex }"
          @click="setVideo(idx)"
        ></button>
      </div>
    </div> -->
  </section>
</template>

<script setup>
import { ref, computed, onMounted, onBeforeUnmount } from 'vue'

const videos = [
  '/Leader360_Homepage_VUE/assets/feature1.mp4',
  '/Leader360_Homepage_VUE/assets/feature2.mp4',
  '/Leader360_Homepage_VUE/assets/feature3.mp4',
  '/Leader360_Homepage_VUE/assets/feature4.mp4'
]
const currentIndex = ref(0)
const currentVideo = computed(() => videos[currentIndex.value])

let timer = null
const setVideo = idx => {
  currentIndex.value = idx
  resetTimer()
}
const nextVideo = () => {
  currentIndex.value = (currentIndex.value + 1) % videos.length
}
const resetTimer = () => {
  clearInterval(timer)
  timer = setInterval(nextVideo, 4000)
}

onMounted(() => {
  timer = setInterval(nextVideo, 4000)
})
onBeforeUnmount(() => {
  clearInterval(timer)
})
</script>

<style scoped>
.hero-main {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 60px 0 40px 0;
  max-width: 1200px;
  margin: 0 auto;
}
.hero-content {
  flex: 1.2;
  padding-right: 40px;
}
.hero-main-label {
  font-size: 1.2em;
  color: #42b883;
  margin-bottom: 8px;
}
.hero-main-title {
  font-size: 1.8em;
  margin: 0 0 16px 0;
  font-weight: bold;
  line-height: 1.1;
}
.hero-main-desc {
  font-size: 1.2em;
  color: #222;
  margin-bottom: 24px;
}
.hero-main-btns {
  display: flex;
  gap: 16px;
  margin-top: 24px;
}
.hero-main-btn {
  padding: 16px 32px;
  border-radius: 32px;
  font-weight: bold;
  text-decoration: none;
  font-size: 1.1em;
  border: 2px solid #fff;
  background: #fff;
  color: #222;
  transition: background 0.2s, color 0.2s;
}
.hero-main-btn.primary {
  background: #fff;
  color: #222;
}
.hero-main-btn:hover {
  background: #42b883;
  color: #fff;
  border-color: #42b883;
}
.hero-video {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
}
.main-video {
  width: 100%;
  max-width: 400px;
  border-radius: 18px;
  box-shadow: 0 4px 32px rgba(0,0,0,0.12);
  background: #222;
}
.video-controls {
  display: flex;
  gap: 10px;
  margin-top: 18px;
  justify-content: center;
}
.video-controls button {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  border: none;
  background: #ccc;
  cursor: pointer;
  transition: background 0.2s;
  outline: none;
  padding: 0;
}
.video-controls button.active,
.video-controls button:hover {
  background: #42b883;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.6s;
}
.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
.hero-bg {
  /* 移除背景色 */
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
</style> 