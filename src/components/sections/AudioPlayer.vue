<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Audio Samples Comparison</h1>
    </el-row>

    <!-- 第一组对比 -->
    <el-row justify="center">
      <h2 class="category-title">Comparison Group 1</h2>
    </el-row>

    <el-row justify="center" class="audio-grid">
      <!-- Mixture -->
      <el-col :xs="4" :sm="3" :md="2" :lg="2" :xl="1">
        <div class="audio-item">
          <h3 class="audio-title">Mixture</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/mix/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
      
      <!-- GT -->
      <el-col :xs="4" :sm="3" :md="2" :lg="2" :xl="1">
        <div class="audio-item">
          <h3 class="audio-title">GT</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/GT/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
      
      <!-- Audio Cue -->
      <el-col :xs="4" :sm="3" :md="2" :lg="2" :xl="1">
        <div class="audio-item">
          <h3 class="audio-title">Audio Cue</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/audio_enr/00003.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
      
      <!-- Visual Cue -->
      <el-col :xs="4" :sm="3" :md="2" :lg="2" :xl="1">
        <div class="audio-item">
          <h3 class="audio-title">Visual Cue</h3>
          <video controls width="100" height="60">
            <source src="/output_audio/baseline_compare_case1/visual_enr/visual_cue.mp4" type="video/mp4">
          </video>
        </div>
      </el-col>
      
      <!-- Model 1-8 -->
      <el-col v-for="i in 8" :key="i" :xs="4" :sm="3" :md="2" :lg="2" :xl="1">
        <div class="audio-item">
          <h3 class="audio-title">Model {{ i }}</h3>
          <audio controls>
 <source src="/output_audio/baseline_compare_case1/audio_enr/00003.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
      
    </el-row>

    

  </div>
</template>

<style scoped>
.section-title {
  font-size: 2rem;
  margin-bottom: 30px;
  color: #2c3e50;
}

.category-title {
  font-size: 1.5rem;
  margin-bottom: 20px;
  color: #3498db;
}

.audio-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
  margin: 0 auto;
  max-width: 1400px;
}

.audio-item {
  background: #f8f9fa;
  border-radius: 8px;
  padding: 12px;
  text-align: center;
  min-width: 100px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
}

.audio-item:hover {
  transform: translateY(-2px);
}

.audio-title {
  font-size: 0.8rem;
  font-weight: 600;
  margin-bottom: 8px;
  color: #2c3e50;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

audio {
  width: 100%;
  height: 30px;
  min-width: 100px;
}

video {
  width: 100px;
  height: 60px;
  border-radius: 4px;
  background: #000;
}

/* 响应式调整 */
@media (max-width: 1200px) {
  .audio-grid {
    gap: 8px;
  }
  
  .audio-item {
    padding: 8px;
    min-width: 90px;
  }
  
  .audio-title {
    font-size: 0.75rem;
  }
}

@media (max-width: 768px) {
  .audio-grid {
    gap: 6px;
  }
  
  .audio-item {
    padding: 6px;
    min-width: 80px;
  }
  
  .audio-title {
    font-size: 0.7rem;
  }
  
  audio {
    height: 25px;
    min-width: 80px;
  }
  
  video {
    width: 80px;
    height: 50px;
  }
}
</style>
