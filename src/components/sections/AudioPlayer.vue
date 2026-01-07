<template>
  <div>
    <el-row justify="center">
      <h1 class="section-title">Audio Samples Comparison</h1>
    </el-row>

    <!-- 第一行：mix.wav, gt.wav -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Reference Samples</h2>
      <el-col :span="8">
        <div class="audio-item">
          <h3 class="audio-title">Mixture</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/mix/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
      <el-col :span="8">
        <div class="audio-item">
          <h3 class="audio-title">GT</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/GT/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
    </el-row>

    <!-- 第二行：audio_enr.wav + 4个模型 -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Audio Enhancement Models</h2>
      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">Audio ENR</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/audio_enr/00003.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">NEMO</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/NEMO/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">LlamaSE-G1</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/LLaSE-G1/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">LauraTSE</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/LLaSE-G1/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">TSE-Omni-A</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/TSE-Omni-A/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>
    </el-row>

    <!-- 第三行：visual_enr.mp4 + 6个模型 -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Visual Enhancement Models</h2>
      <el-col :span="3">
        <div class="audio-item video-item">
          <h3 class="audio-title">Visual ENR</h3>
          <video controls class="video-player">
            <source src="/output_audio/baseline_compare_case1/visual_enr/visual_cue.mp4" type="video/mp4">
          </video>
        </div>
      </el-col>

      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">USEV</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/USEV/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>


      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">AV-Mamba</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/AV-Mamba/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>

      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">AV-Sepformer</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/AV-Sepformer/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>

      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">AV-DIFFUSE</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/AV-DIFFUSE/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>


      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">FLOWAVSE</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/FLOWAVSE/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>


      <el-col :span="4">
        <div class="audio-item">
          <h3 class="audio-title">TSE-Omni-V</h3>
          <audio controls>
            <source src="/output_audio/baseline_compare_case1/TSE-Omni-V/test_test_HiwJ0hNl1Fw_00002_0_test_VSLurJfOSiA_00001_7.835460015641594_4.096.wav" type="audio/wav">
          </audio>
        </div>
      </el-col>

 

    </el-row>
  </div>
</template>

<script>
export default {
  name: 'AudioComparison'
}
</script>

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

.audio-item {
  background: #f8f9fa;
  border-radius: 8px;
  padding: 15px;
  text-align: center;
  min-width: 120px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.video-item {
  min-width: 150px;
}

.audio-title {
  font-size: 0.9rem;
  font-weight: 600;
  margin-bottom: 10px;
  color: #2c3e50;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

audio {
  width: 100%;
  height: 35px;
  min-width: 120px;
}

.video-player {
  width: 140px;
  height: 80px;
  border-radius: 6px;
  background: #000;
  object-fit: cover;
}

/* 响应式调整 */
@media (max-width: 1200px) {
  .audio-item {
    min-width: 110px;
    padding: 12px;
  }
  
  .video-player {
    width: 120px;
    height: 70px;
  }
}

@media (max-width: 768px) {
  .audio-row {
    gap: 10px;
  }
  
  .audio-item {
    min-width: 100px;
    padding: 10px;
  }
  
  .video-player {
    width: 100px;
    height: 60px;
  }
  
  .audio-title {
    font-size: 0.8rem;
  }
}

@media (max-width: 480px) {
  .audio-item {
    min-width: 90px;
    padding: 8px;
  }
  
  .video-player {
    width: 90px;
    height: 50px;
  }
  
  audio {
    height: 30px;
  }
}
</style>
