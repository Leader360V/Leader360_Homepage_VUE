<template>
  <section id="model-architecture" class="model-architecture model-arch-bg">
    <div class="container">
      <div class="model-arch-label">Model architecture</div>
      <h2 class="model-arch-title">Meta Segment Anything Model 2 design</h2>
      <p class="model-arch-desc">
        The SAM 2 model extends the promptable capability of SAM to the video domain by adding a per session memory module that captures information about the target object in the video. This allows SAM 2 to track the selected object throughout all video frames, even if the object temporarily disappears from view, as the model has context of the object from previous frames. SAM 2 also supports the ability to make corrections in the mask prediction based on additional prompts on any frame.
      </p>
      <p class="model-arch-desc">
        SAM 2's streaming architecture—which processes video frames one at a time—is also a natural generalization of SAM to the video domain. When SAM 2 is applied to images, the memory module is empty and the model behaves like SAM.
      </p>
    </div>
  </section>
</template>

<script setup>
// 暂无逻辑
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
</style> 