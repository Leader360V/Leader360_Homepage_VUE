<template>
  <section class="features features-bg">
    <h2>Multiple Scenarios</h2>
    <div class="feature-grid">
      <div class="about-card-sm-gradient">
        <div class="about-card-sm">
          <div class="about-card-sm-media">
            <video src="/assets/feature3.mp4" autoplay loop muted playsinline controls class="about-card-sm-video"></video>
          </div>
          <div class="about-card-sm-content">
            <h3 class="about-card-sm-title">Seamless Translation</h3>
            <div class="about-card-sm-desc">
              Hear what you sound like in another language.
            </div>
            <div class="about-card-sm-tag">Language AI</div>
            <a class="about-card-sm-btn" href="#">Try it <span class="about-card-btn-arrow">↗</span></a>
          </div>
        </div>
      </div>
      <div class="about-card-sm-gradient">
        <div class="about-card-sm">
          <div class="about-card-sm-media">
            <video src="/assets/feature4.mp4" autoplay loop muted playsinline controls class="about-card-sm-video"></video>
          </div>
          <div class="about-card-sm-content">
            <h3 class="about-card-sm-title">Animated Drawings</h3>
            <div class="about-card-sm-desc">
              Bring hand-drawn sketches to life with animations.
            </div>
            <div class="about-card-sm-tag vision">Vision AI</div>
            <a class="about-card-sm-btn" href="#">Try it <span class="about-card-btn-arrow">↗</span></a>
          </div>
        </div>
      </div>
      <div class="about-card-sm-gradient">
        <div class="about-card-sm">
          <div class="about-card-sm-media">
            <video src="/assets/feature1.mp4" autoplay loop muted playsinline controls class="about-card-sm-video"></video>
          </div>
          <div class="about-card-sm-content">
            <h3 class="about-card-sm-title">Audiobox</h3>
            <div class="about-card-sm-desc">
              Create an audio story with AI-generated voices and sounds.
            </div>
            <div class="about-card-sm-tag">Language AI</div>
            <a class="about-card-sm-btn" href="#">Try it <span class="about-card-btn-arrow">↗</span></a>
          </div>
        </div>
      </div>
      <!-- <FeatureCard
        v-for="(feature, idx) in features"
        :key="idx"
        :title="feature.title"
        :desc="feature.desc"
        :video="feature.video"
      /> -->
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
  gap: 10px;
  margin-top: 32px;
}
.features-bg {
  background: #f7f8fa;
}




.about-card {
  max-width: 1200px;
  margin: 0 auto 48px auto;
  background: #fff !important;
  border-radius: 28px;
  display: flex;
  align-items: stretch;
  gap: 0;
  box-shadow: 0 2px 16px rgba(0,0,0,0.08);
  overflow: hidden;
}
.about-card-media {
  flex: 1.2;
  display: flex;
  align-items: center;
  justify-content: center;
  background: #fff;
  min-width: 320px;
  position: relative;
}
.about-card-media-inner {
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
}
.about-video {
  width: 100%;
  max-width: 340px;
  border-radius: 18px;
  margin: 32px 0 32px 32px;
  background: #fff;
  box-shadow: 0 2px 16px rgba(0,0,0,0.18);
}
.about-card-content {
  flex: 2;
  padding: 48px 48px 48px 32px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.about-card-title {
  font-size: 2.1rem;
  font-weight: 700;
  margin-bottom: 18px;
  color: #111;
}
.about-card-desc {
  font-size: 1.18rem;
  color: #333;
  margin-bottom: 18px;
  line-height: 1.5;
}
.about-card-tag {
  color: #ffe066;
  font-weight: 600;
  font-size: 1.1rem;
  margin-bottom: 28px;
}
.about-card-btn {
  display: inline-flex;
  align-items: center;
  background: #fff;
  color: #111;
  border-radius: 999px;
  padding: 12px 32px;
  font-size: 1.1rem;
  font-weight: 600;
  text-decoration: none;
  border: 1.5px solid #111;
  min-width: 120px;
  min-height: 44px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.04);
  transition: background 0.2s, color 0.2s;
  margin-top: 8px;
}
.about-card-btn:hover {
  background: #111;
  color: #fff;
}
.about-card-btn-arrow {
  font-size: 1.2em;
  margin-left: 8px;
}
@media (max-width: 900px) {
  .about-header {
    padding: 32px 0 18px 0;
  }
  .about-title {
    font-size: 1.3rem;
  }
  .about-card {
    flex-direction: column;
    border-radius: 18px;
  }
  .about-card-media {
    min-width: 0;
    justify-content: flex-start;
  }
  .about-card-media-inner {
    justify-content: center;
  }
  .about-video {
    margin: 24px auto 0 auto;
    max-width: 90vw;
  }
  .about-card-content {
    padding: 24px 16px 32px 16px;
  }
}
.about-cards-row {
  display: flex;
  gap: 32px;
  max-width: 1200px;
  margin: 0 auto 30px auto;
  justify-content: center;
  flex-wrap: wrap;
}
.about-card-sm-gradient {
  border-radius: 24px;
  padding: 2px;
  background: transparent;
  transition: background 0.2s, box-shadow 0.2s;
}
.about-card-sm-gradient:hover {
  background: linear-gradient(90deg, #e05297 10%, #6c63ff 40%, #2ec4b6 70%, #ffe066 100%);
  box-shadow: 0 4px 24px rgba(0,0,0,0.18);
}
.about-card-sm {
  background: #fff !important;
  border-radius: 24px;
  box-shadow: 0 2px 16px rgba(0,0,0,0.12);
  overflow: hidden;
  width: 350px;
  display: flex;
  flex-direction: column;
  align-items: stretch;
  position: relative;
  padding-bottom: 24px;
  border: none;
  transition: box-shadow 0.2s;
}
.about-card-sm-gradient:not(:hover) .about-card-sm {
  box-shadow: 0 2px 16px rgba(0,0,0,0.12);
}
.about-card-sm-media {
  width: 100%;
  background: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 18px 0 0 0;
}
.about-card-sm-video {
  width: 90%;
  border-radius: 16px;
  background: #fff;
}
.about-card-sm-content {
  padding: 18px 24px 0 24px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.about-card-sm-title {
  font-size: 1.3rem;
  font-weight: 700;
  margin-bottom: 8px;
  color: #111;
}
.about-card-sm-desc {
  font-size: 1rem;
  color: #333;
  margin-bottom: 10px;
  line-height: 1.5;
}
.about-card-sm-tag {
  color: #2ec4b6;
  font-weight: 600;
  font-size: 1rem;
  margin-bottom: 18px;
}
.about-card-sm-tag.vision {
  color: #ffe066;
}
.about-card-sm-btn {
  display: inline-flex;
  align-items: center;
  background: #fff;
  color: #111;
  border-radius: 999px;
  padding: 10px 24px;
  font-size: 1rem;
  font-weight: 600;
  text-decoration: none;
  border: 1.5px solid #111;
  min-width: 90px;
  min-height: 36px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.04);
  transition: background 0.2s, color 0.2s;
}
.about-card-sm-btn:hover {
  background: #111;
  color: #fff;
}
@media (max-width: 1200px) {
  .about-cards-row {
    gap: 18px;
  }
  .about-card-sm {
    width: 320px;
  }
}
@media (max-width: 900px) {
  .about-cards-row {
    flex-direction: column;
    align-items: center;
    gap: 18px;
  }
  .about-card-sm {
    width: 95vw;
    min-width: 0;
  }
}
</style> 