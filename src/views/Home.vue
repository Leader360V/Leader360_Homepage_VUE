<template>
  <div class="home">
    <HeroMain />
    <Features />
    <Research />
    <!-- <VideoSlider /> -->
    <ModelArchitecture />
    <Dataset />
    <OpenInnovation />
    <Resources />
  </div>
</template>

<script setup>
import HeroMain from '../components/HeroMain.vue'
import Features from '../components/Features.vue'
import Research from '../components/Research.vue'
// import VideoSlider from '../components/VideoSlider.vue'
import ModelArchitecture from '../components/ModelArchitecture.vue'
import Dataset from '../components/Dataset.vue'
import OpenInnovation from '../components/OpenInnovation.vue'
import Resources from '../components/Resources.vue'
</script>

<style scoped>
.home {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  background: #fff;
  min-height: 100vh;
  box-sizing: border-box;
  padding-left: 16px;
  padding-right: 16px;
}
</style> 