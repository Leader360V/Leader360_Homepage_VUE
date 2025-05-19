<template>
  <div class="feature-card">
    <video :src="video" autoplay loop muted playsinline></video>
    <h3>{{ title }}</h3>
    <p>{{ desc }}</p>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  desc: String,
  video: String
})
</script>

<style scoped>
.feature-card {
  background: #fff;
  border-radius: 16px;
  box-shadow: 0 2px 16px rgba(0,0,0,0.08);
  padding: 24px;
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.feature-card video {
  width: 100%;
  max-width: 240px;
  border-radius: 12px;
  margin-bottom: 16px;
}
.feature-card h3 {
  margin: 0 0 8px 0;
  font-size: 1.2em;
}
.feature-card p {
  color: #555;
  font-size: 1em;
}
</style> 