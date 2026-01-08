<script setup>
import { ref } from 'vue'

const selectedCase = ref('case1') // 只需要这一行
</script>

<template>
  <div>
    <el-row justify="center">
      <h1 class="section-title">Baseline Comparison</h1>
    </el-row>

    <!-- Case选择器 -->
    <el-row justify="center" class="case-selector">
      <el-radio-group v-model="selectedCase">
        <el-radio-button label="case1">Case 1</el-radio-button>
        <el-radio-button label="case2">Case 2</el-radio-button>
      </el-radio-group>
    </el-row>
    

    <!-- Case 1 的内容 -->
    <div v-if="selectedCase === 'case1'">

    <!-- 第一行：mix.wav, gt.wav -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title"> Sample 1 </h2>
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
      <h2 class="row-title">Audio Cue Based Models</h2>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Audio Cue</div>
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
      <h2 class="row-title">Visual Cue Based Models</h2>
      <el-col :span="3">
        <el-container class="video-container">
          <div class="audio-title">Visual Cue</div>
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

    </el-row>
          <!-- 第4行：visual_enr.mp4 + 6个模型 -->
    <el-row justify="center" class="audio-row">

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

         <!-- Case 2 的内容 -->
    <div v-if="selectedCase === 'case2'">

     <!-- 第一行：mix.wav, gt.wav -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title"> Sample 2 </h2>
      <el-col :span="8">
        <el-container class="video-container">
          <div class="audio-title">Mixture</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/mix/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="8">
        <el-container class="video-container">
          <div class="audio-title">GT</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/GT/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
    </el-row>

    <!-- 第二行：audio_enr.wav + 4个模型 -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Audio Cue Based Models</h2>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Audio Cue</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/audio_enr/00001.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">NEMO</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/NEMO/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">LlamaSE-G1</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/LLaSE-G1/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">LauraTSE</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/LauraTSE/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">TSE-Omni-A</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/TSE-Omni-A/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
    </el-row>

    <!-- 第三行：visual_enr.mp4 + 6个模型 -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Visual Cue Based Models</h2>
      <el-col :span="3">
        <el-container class="video-container">
          <div class="audio-title">Visual Cue</div>
          <video controls muted preload playsinline>
            <source src="/output_audio/baseline_compare_case2/visual_enr/visual_cue_h264.mp4" type="video/mp4">
          </video>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">USEV</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/USEV/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">AV-Mamba</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/AV-Mamba/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
 

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">AV-Sepformer</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/AV-Sepformer/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

       </el-row>
          <!-- 第4行：visual_enr.mp4 + 6个模型 -->
    <el-row justify="center" class="audio-row">
      
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">AV-DIFFUSE</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/AV-DIFFUSE/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">FLOWAVSE</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/FLOWAVSE/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">TSE-Omni-V</div>
          <audio controls>
            <source src="/output_audio/baseline_compare_case2/TSE-Omni-V/test_test_UmvOgW6iV2s_00007_0_test_FxtSMZKMdes_00009_-8.579278836042262_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
    </el-row>
    </div>

    ##############################################
     <!-- 新的Visual Corruption Section -->
    <el-divider />
    <el-row justify="center">
      <h1 class="section-title">Visual Corruption</h1>
    </el-row>

    <!-- Sample 1 -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Sample 1</h2>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Mixture</div>
          <audio controls>
            <source src="/output_audio/vocc/mix/test_test_qYUmI5kGsYk_00001_0_test_GMynksvCcUI_00009_-8.634935336137668_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">GT</div>
          <audio controls>
            <source src="/output_audio/vocc/GT/test_test_qYUmI5kGsYk_00001_0_test_GMynksvCcUI_00009_-8.634935336137668_4.288.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      </el-row>

    <!-- Sample 2 -->
    <el-row justify="center" class="audio-row">
      
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Visual Cue</div>
          <video controls muted preload playsinline>
            <source src="/output_audio/vocc/visual_enr/visual_cue_h264.mp4" type="video/mp4">
          </video>
        </el-container>
      </el-col>

        <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Visual Cue(Intact)</div>
          <video controls muted preload playsinline>
            <source src="/output_audio/vocc/visual_enr/visual_cue_clean_h264.mp4" type="video/mp4">
          </video>
        </el-container>
      </el-col>
      
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">USEV</div>
          <audio controls>
            <source src="/output_audio/vocc/USEV/test_test_qYUmI5kGsYk_00001_0_test_GMynksvCcUI_00009_-8.634935336137668_4.288_mask1_start53_len42.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">TSE-Omni-V</div>
          <audio controls>
            <source src="/output_audio/vocc/TSE-Omni-V/test_test_qYUmI5kGsYk_00001_0_test_GMynksvCcUI_00009_-8.634935336137668_4.288_mask1_start53_len42.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
    </el-row>

    <!-- Sample 2 -->
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Sample 2</h2>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Mixture</div>
          <audio controls>
            <source src="/output_audio/vonly1s/mix/test_test_TVtgb153S6I_00001_0_test_V1yW5IsnSjo_00001_-0.52783909452579_6.08.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">GT</div>
          <audio controls>
            <source src="/output_audio/vonly1s/GT/test_test_TVtgb153S6I_00001_0_test_V1yW5IsnSjo_00001_-0.52783909452579_6.08.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
         </el-row>

    <!-- Sample 2 -->
    <el-row justify="center" class="audio-row">
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Visual Cue</div>
          <video controls muted preload playsinline>
            <source src="/output_audio/vonly1s/visual_enr/visual_cue_h264.mp4" type="video/mp4">
          </video>
        </el-container>
      </el-col>
           <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Visual Cue(Intact)</div>
          <video controls muted preload playsinline>
            <source src="/output_audio/vonly1s/visual_enr/visual_cue_clean_h264.mp4" type="video/mp4">
          </video>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">USEV</div>
          <audio controls>
            <source src="/output_audio/vonly1s/USEV/test_test_TVtgb153S6I_00001_0_test_V1yW5IsnSjo_00001_-0.52783909452579_6.08_mask2_start75_len4.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">ImageNet</div>
          <audio controls>
            <source src="/output_audio/vonly1s/ImagineNET/test_test_TVtgb153S6I_00001_0_test_V1yW5IsnSjo_00001_-0.52783909452579_6.08_mask2_start75_len4.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">TSE-Omni-V</div>
          <audio controls>
            <source src="/output_audio/vonly1s/TSE-Omni-V/test_test_TVtgb153S6I_00001_0_test_V1yW5IsnSjo_00001_-0.52783909452579_6.08_mask0_start0_len95_test_ds_rate25.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
    </el-row>
    ##############################################



     ##############################################
     <!-- 新的 Streaming Inference -->
    <el-divider />
    <el-row justify="center">
      <h1 class="section-title">Streaming Inference</h1>
    </el-row>

    <!-- Sample 1 -->
    <el-row justify="center" class="audio-row">
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Mixture</div>
          <audio controls>
            <source src="/output_audio/streaming/mix/test_test_sxnlvwprfSc_all_concat_0_test_1bnzVjOJ6NM_all_concat_7.82_10.69.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">GT</div>
          <audio controls>
            <source src="/output_audio/streaming/GT/test_test_sxnlvwprfSc_all_concat_0_test_1bnzVjOJ6NM_all_concat_7.82_10.69.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      </el-row>

    <!-- Sample 2 -->
 

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Audio Cue</div>
          <video controls muted preload playsinline>
            <source src="/output_audio/streaming/audio_enr/test_test_sxnlvwprfSc_streaming_enr.wav" type="video/mp4">
          </video>
        </el-container>
      </el-col>

       <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">LauraTSE</div>
          <audio controls>
            <source src="/output_audio/streaming/LauraTSE/test_test_sxnlvwprfSc_all_concat_0_test_1bnzVjOJ6NM_all_concat_7.82_10.69.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">TSE-Omni-A</div>
          <audio controls>
            <source src="/output_audio/streaming/TSE-Omni-A/test_test_sxnlvwprfSc_all_concat_0_test_1bnzVjOJ6NM_all_concat_7.82_10.69.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

        <el-row justify="center" class="audio-row">
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Visual Cue</div>
          <video controls muted preload playsinline>
            <source src="/output_audio/streaming/visual_enr/visual_cue_h264.mp4" type="video/mp4">
          </video>
        </el-container>
      </el-col>

      
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">TSE-Omni-V</div>
          <audio controls>
            <source src="/output_audio/streaming/TSE-Omni-V/test_test_sxnlvwprfSc_all_concat_0_test_1bnzVjOJ6NM_all_concat_7.82_10.69.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
    </el-row>
    ##############################################


     ##############################################
     <!-- 新的 target speaker switch -->
    <el-divider />
    <el-row justify="center">
      <h1 class="section-title"> Target Speaker Switch </h1>
    </el-row>

    <!-- Sample 1 -->
    <el-row justify="center" class="audio-row">
          <h2 class="row-title">Sample 1</h2>
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Mixture</div>
          <audio controls>
            <source src= "/output_audio/switch/mix/test_test_UAj1hsXp18c_00022_0_test_eZj5n8ScTkI_00005_-2.6283_test_mgcjr1yz7ow_00006_6.4424_3.776_3.09.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">GT</div>
          <audio controls>
            <source src= "/output_audio/switch/GT/test_test_UAj1hsXp18c_00022_0_test_eZj5n8ScTkI_00005_-2.6283_test_mgcjr1yz7ow_00006_6.4424_3.776_3.09.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

         <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title"> Visual Cue </div>
          <audio controls>
            <source src= "/output_audio/switch/visual_enr/test_test_UAj1hsXp18c_00022_0_test_eZj5n8ScTkI_00005_-2.6283_test_mgcjr1yz7ow_00006_6.4424_3.776_3.09_visual_cue_h264.mp4" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      
         <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title"> TSE-Omni-V </div>
          <audio controls>
            <source src= "/output_audio/switch/TSE-Omni-V/test_test_UAj1hsXp18c_00022_0_test_eZj5n8ScTkI_00005_-2.6283_test_mgcjr1yz7ow_00006_6.4424_3.776_3.09_switch_time3.09.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      
      </el-row>

    <!-- Sample 2 -->
 
    <el-row justify="center" class="audio-row">
      <h2 class="row-title">Sample 2</h2>
         
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Mixture</div>
          <audio controls>
            <source src= "/output_audio/switch/mix/test_test_Us70DN2XSfM_00003_0_test_7OMLSs8t1ng_00010_8.7783_test_dYNc3P4jSt4_00006_7.3216_3.136_3.4.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">GT</div>
          <audio controls>
            <source src= "/output_audio/switch/GT/test_test_Us70DN2XSfM_00003_0_test_7OMLSs8t1ng_00010_8.7783_test_dYNc3P4jSt4_00006_7.3216_3.136_3.4.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      
         <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title"> Visual Cue </div>
          <audio controls>
            <source src= "/output_audio/switch/visual_enr/test_test_Us70DN2XSfM_00003_0_test_7OMLSs8t1ng_00010_8.7783_test_dYNc3P4jSt4_00006_7.3216_3.136_3.4_visual_cue_h264.mp4" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      
         <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title"> TSE-Omni-V </div>
          <audio controls>
            <source src= "/output_audio/switch/TSE-Omni-V/test_test_Us70DN2XSfM_00003_0_test_7OMLSs8t1ng_00010_8.7783_test_dYNc3P4jSt4_00006_7.3216_3.136_3.4_switch_time3.4.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>



      <el-row justify="center" class="audio-row">
      <h2 class="row-title">Sample 3</h2>
         
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">Mixture</div>
          <audio controls>
            <source src= "/output_audio/switch/mix/test_test_psN1DORYYV0_00020_0_test_ZJNESMhIxQ0_00013_4.5693_test_JSSc7hYKstI_00015_5.3053_3.648_3.44.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      
      <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title">GT</div>
          <audio controls>
            <source src= "/output_audio/switch/GT/test_test_psN1DORYYV0_00020_0_test_ZJNESMhIxQ0_00013_4.5693_test_JSSc7hYKstI_00015_5.3053_3.648_3.44.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>

      
         <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title"> Visual Cue </div>
          <audio controls>
            <source src= "/output_audio/switch/visual_enr/test_test_psN1DORYYV0_00020_0_test_ZJNESMhIxQ0_00013_4.5693_test_JSSc7hYKstI_00015_5.3053_3.648_3.44_visual_cue_h264.mp4" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
      
         <el-col :span="4">
        <el-container class="video-container">
          <div class="audio-title"> TSE-Omni-V </div>
          <audio controls>
            <source src= "/output_audio/switch/TSE-Omni-V/test_test_psN1DORYYV0_00020_0_test_ZJNESMhIxQ0_00013_4.5693_test_JSSc7hYKstI_00015_5.3053_3.648_3.44_switch_time3.44.wav" type="audio/wav">
          </audio>
        </el-container>
      </el-col>
        </el-row>
    
       
    ##############################################


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
  width: 224px;
  height: 224px;
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
