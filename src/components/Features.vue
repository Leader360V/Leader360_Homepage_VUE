<template>
  <section class="features features-bg">
    <h2>Features</h2>
    <div class="feature-grid">
      <FeatureCard
        v-for="(feature, idx) in features"
        :key="idx"
        :title="feature.title"
        :desc="feature.desc"
        :video="feature.video"
      />
    </div>
  </section>
</template>

<script setup>
import FeatureCard from './FeatureCard.vue'

const features = [
  {
    title: 'Select objects and make adjustments across video frames',
    desc: 'Using SAM 2, you can select one or multiple objects in a video frame. Use additional prompts to refine the model predictions.',
    video: '/assets/feature1.mp4'
  },
  {
    title: 'Robust segmentation, even in unfamiliar videos',
    desc: 'SAM 2 is capable of strong zero-shot performance for objects, images and videos not previously seen during model training, enabling use in a wide range of real-world applications.',
    video: '/assets/feature2.mp4'
  },
  {
    title: 'Real-time interactivity and results',
    desc: 'SAM 2 is designed for efficient video processing with streaming inference to enable real-time, interactive applications.',
    video: '/assets/feature3.mp4'
  }
]
</script>

<style scoped>
.features {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 0;
}
.feature-grid {
  display: flex;
  gap: 32px;
  margin-top: 32px;
}
.features-bg {
  background: #f7f8fa;
}
</style> 