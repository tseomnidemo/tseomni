<script setup>
import { ref } from 'vue'

const selectedCase = ref('case1') // 只需要添加这一行
</script>

<template>
  <div>
    <el-row justify="center">
      <h1 class="section-title">Audio Samples Comparison</h1>
    </el-row>

    <!-- 只需要添加这个选择器 -->
    <el-row justify="center" class="case-selector">
      <el-radio-group v-model="selectedCase">
        <el-radio-button label="Case1">Case 1</el-radio-button>
        <el-radio-button label="Case2">Case 2</el-radio-button>
      </el-radio-group>
    </el-row>

    <!-- 第一行：mix.wav, gt.wav -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Reference Samples</h2>
      <el-col :span="8">
        <el-container class="video-container">
          <div class="audio-title">Mixture</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/mix/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="8">
        <el-container class="video-container">
          <div class="audio-title">GT</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/GT/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
    </el-row>

    <!-- 第二行：audio_enr.wav + 4个模型 -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Audio Enhancement Models</h2>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Audio ENR</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/audio_enr/00003.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">NEMO</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/NEMO/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">LlamaSE-G1</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/LLaSE-G1/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">LauraTSE</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/LauraTSE/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">TSE-Omni-A</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/TSE-Omni-A/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
    </el-row>

    <!-- 第三行：visual_enr.mp4 + 6个模型 -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Visual Enhancement Models</h2>
      <el-col :span="3">
        <el-container class="video-container">
          <div class="audio-title">Visual ENR</div>
          <video controls muted preload playsinline>
            <source src="/output_audio/baseline_compare_case1/visual_enr/visual_cue_h264.mp4" type="video/mp4">
          </video>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">USEV</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/USEV/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">AV-Mamba</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/AV-Mamba/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">AV-Sepformer</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/AV-Sepformer/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">AV-DIFFUSE</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/AV-DIFFUSE/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">FLOWAVSE</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/FLOWAVSE/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">TSE-Omni-V</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/TSE-Omni-V/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
    </el-row>
  </div>
</template>


<style scoped>
.section-title {
  font-size: 2rem;
  margin-bottom: 30px;
  color: #2c3e50;
  text-align: center;
}

.row-title {
  font-size: 1.3rem;
  margin: 30px 0 20px 0;
  color: #3498db;
  text-align: center;
  width: 100%;
}

.audio-row {
  margin: 20px 0;
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 15px;
}

.video-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 10px 0;
}

.audio-title {
  margin-bottom: 5px;
  font-weight: bold;
  font-size: 16px;
  text-align: center;
  color: #2c3e50;
}

audio {
  width: 100%;
  height: 35px;
  min-width: 120px;
}

video {
  aspect-ratio: 16/9;
  /* width: 200px; */
  /* width: 80%; */
  width: 320px;
  height: 320px;
  border-radius: 6px;
  background: #000;
  object-fit: cover;
}

/* 响应式调整 */
@media (max-width: 1200px) {
  video {
    width: 180px;
  }
  
  .audio-title {
    font-size: 14px;
  }
}

@media (max-width: 768px) {
  .audio-row {
    gap: 10px;
  }
  
  video {
    width: 150px;
  }
  
  .audio-title {
    font-size: 12px;
  }
}

@media (max-width: 480px) {
  video {
    width: 120px;
  }
  
  audio {
    height: 30px;
  }
  
  .audio-title {
    font-size: 11px;
  }
}
</style>
