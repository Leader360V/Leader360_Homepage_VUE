<template>
  <section id="research" class="research">
    <div class="container research-flex">
      <div class="research-left">
        <h2>Why Collect Additional Videos by Ourselves?</h2>
        <p class="research-desc">
          The existing datasets exhibit imbalances in scene diversity. This is evident in three key aspects.  
        </p>
        <div class="research-highlights-box">
          <div class="research-highlights-title"><b>Highlights</b></div>
          <ul class="research-highlights-list">
            <li>There is a significant imbalance in the ratio of indoor to outdoor videos within the dataset, as well as in the distribution of various types of labels.</li>
            <li>The ratio of dynamically shot videos to stationary ones is unbalanced.</li>
            <li>Among the dynamically shot videos, the ratio of videos featuring human subjects versus those featuring vehicles (including cars, drones, etc.) is also significantly skewed.</li>
          </ul>
        </div>
      </div>
      <!-- <div class="research-right">
        <video class="research-video" src="/assets/demo.mp4" autoplay loop muted playsinline controls></video>
      </div> -->
      <div class="hero-video">
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
    </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed, onMounted, onBeforeUnmount } from 'vue'

const videos = [
  '/Leader360_Homepage_VUE/assets/videos/Gym-Indoor.mp4',
  '/Leader360_Homepage_VUE/assets/videos/Road-Outdoor.mp4',
  '/Leader360_Homepage_VUE/assets/videos/Basement-Indoor.mp4',
  '/Leader360_Homepage_VUE/assets/videos/SubwayStation-Indoor.mp4'
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
</style> 