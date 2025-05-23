<template>
  <section id="model-architecture" class="model-architecture model-arch-bg">
    <div class="container">
      <!-- <div class="model-arch-label">Model architecture</div> -->
      <h2 class="model-arch-title">Automatic Annotate Any 360 Video Pipeline</h2>
      <p class="model-arch-desc">
        Introduction
      </p>
      <!-- <p class="model-arch-desc">
        SAM 2's streaming architecture—which processes video frames one at a time—is also a natural generalization of SAM to the video domain. When SAM 2 is applied to images, the memory module is empty and the model behaves like SAM.
      </p> -->
    </div>

    <div class="carousel results-carousel">
      <button @click="prevGroup" class="carousel-arrow left-arrow">←</button>
      <div class="video-group">
        <div 
          class="box m-5"
          v-for="(item, index) in currentGroup"
          :key="index"
        >
          <video 
            :src="item.src" 
            :alt="item.altText"
            width="80%"
            autoplay loop muted playsinline controls
          ></video>
          <p>{{ item.description }}</p>
        </div>
      </div>
      <button @click="nextGroup" class="carousel-arrow right-arrow">→</button>
    </div>

  </section>
</template>

<script setup>
import { ref, computed } from 'vue';

const carouselItems = ref([
  {
    src: "/Leader360_Homepage_VUE/assets/feature1.mp4",
    altText: "Home",
    description: "Interior home snapshot"
  },
  {
    src: "/Leader360_Homepage_VUE/assets/feature2.mp4",
    altText: "Hotel",
    description: "Hotel scenario"
  },
  {
    src: "/Leader360_Homepage_VUE/assets/feature3.mp4",
    altText: "Park",
    description: "Park view"
  },
  {
    src: "/Leader360_Homepage_VUE/assets/feature4.mp4",
    altText: "Beach",
    description: "Beach scene"
  },
  {
    src: "/Leader360_Homepage_VUE/assets/feature1.mp4",
    altText: "City",
    description: "City skyline"
  },
  {
    src: "/Leader360_Homepage_VUE/assets/feature2.mp4",
    altText: "Forest",
    description: "Forest trail"
  }
]);

const currentIndex = ref(0);
const videosPerGroup = 3;

const currentGroup = computed(() => {
  const start = currentIndex.value * videosPerGroup;
  return carouselItems.value.slice(start, start + videosPerGroup);
});

function prevGroup() {
  if (currentIndex.value > 0) {
    currentIndex.value--;
  }
}

function nextGroup() {
  if ((currentIndex.value + 1) * videosPerGroup < carouselItems.value.length) {
    currentIndex.value++;
  }
}
</script>

<style scoped>
.model-architecture {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 0;
}
.model-arch-label {
  font-size: 1.2em;
  color: #42b883;
  margin-bottom: 8px;
}
.model-arch-title {
  font-size: 2em;
  margin: 0 0 16px 0;
}
.model-arch-desc {
  font-size: 1.2em;
  color: #555;
  margin-bottom: 16px;
}
.model-arch-bg {
  background: #f7f8fa;
}
.carousel {
  display: flex;
  align-items: center;
}
.carousel-arrow {
  background: none;
  border: none;
  font-size: 2em;
  cursor: pointer;
}
.video-group {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 5px
}
.box {
  flex: 1 0 40%;  /* 每个视频占据30%的宽度 */
  margin: 1px;   /* 添加间距 */
  text-align: center;
  /* gap: 5px */
}

</style> 