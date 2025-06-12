<template>
  <section id="dataset" class="dataset-section">
    <div class="container dataset-flex">
      <div class="dataset-left">
        <!-- <video class="dataset-video" src="/assets/feature4.mp4" autoplay loop muted playsinline controls></video> -->
         <img class="dataset-video" src="/assets/img/Framework_00.png">
      </div>
      <div class="dataset-right">
        <!-- <div class="dataset-label">The Segment Anything Video Dataset</div> -->
        <h2 class="dataset-title">Automatic Annotate Any 360 Video Pipeline</h2>
        
        <p class="dataset-desc">
          This pipeline is an automatic labeling pipeline, which subtly coordinates pre-trained 2D segmentors and large language models (LLMs) to facilitate the labeling. The pipeline operates in three novel stages.
        </p>
        <!-- <div class="dataset-highlights-box">
          <div class="dataset-highlights-title"><b>Highlights</b></div>
          <ul class="dataset-highlights-list">
            <li>Initial Annotation Phase: We first extract keyframes and use multiple 2D segmentors (e.g., CropFormer , OneFormer) to generate semantic and instance segmentation proposals. These outputs are unified and aligned via LLM-based semantic matching, then refined through a Semantic- and Distortion-aware Refinement (SDR) Module that leverages SAM2 to produce high-quality panoramic masks.</li>
            <li>Auto-Refine Annotation Phase: For subsequent keyframes in the video, we iteratively propagate annotations and identify low-quality regions based on mask coverage. Frames failing coverage thresholds are reprocessed using a GPT-guided Motion-Continuity Refinement (MCR) module, which resolves annotation inconsistencies across left-right ERP and recovers missing masks caused by occlusion or distortion.</li>
            <li>Manual Revise Phase: Finally, human annotators validate and correct the outputs from the previous stages. Multi-annotator review ensures consistency and completeness across frames, producing the final high-quality annotations.</li>
          </ul>
        </div> -->
        <!-- <p class="dataset-desc">
          Please email <a href="mailto:support@segment-anything.com" class="dataset-mail">support@segment-anything.com</a> with any issues or questions regarding the SA-V dataset.
        </p> -->
        <!-- <a class="dataset-link" href="#" target="_blank">
          <span class="arrow">&#8594;</span>
          <span>Explore the dataset</span>
        </a> -->
      </div>
    </div>
  </section>
</template>

<script setup>
// 暂无逻辑
</script>

<style scoped>
.dataset-section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 0;
}
.dataset-flex {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 2rem;
}
.dataset-left {
  flex: 2;
  max-width: 80%;
  display: flex;
  justify-content: center;
}
.dataset-right {
  flex: 1;
  padding-left: 20px;
}
.dataset-video {
  width: 100%;
  /* max-width: 400px; */
  border-radius: 18px;
  box-shadow: 0 4px 32px rgba(0,0,0,0.12);
}
.dataset-label {
  font-size: 1.2em;
  color: #42b883;
  margin-bottom: 8px;
}
.dataset-title {
  font-size: 2em;
  margin: 0 0 16px 0;
}
.dataset-desc {
  font-size: 1.2em;
  color: #555;
  margin-bottom: 16px;
}
.dataset-mail {
  color: #42b883;
  text-decoration: underline;
}
.dataset-link {
  display: inline-block;
  margin-top: 18px;
  color: #42b883;
  font-weight: bold;
  text-decoration: underline;
}
.dataset-highlights-box {
  background: #f9f9f9;
  border-radius: 12px;
  padding: 16px;
  margin-top: 24px;
  text-align: left;
}
.dataset-highlights-title {
  font-size: 1.2em;
  margin-bottom: 8px;
}
.dataset-highlights-list {
  list-style-type: disc;
  padding-left: 20px;
}
</style> 