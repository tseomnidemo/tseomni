<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Audio Samples Comparison</title>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap">
    <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/axios@1.1.2/dist/axios.min.js"></script>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: #333;
            background: linear-gradient(135deg, #f5f7fa 0%, #e4efe9 100%);
            padding: 20px;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1800px;
            margin: 0 auto;
            background: white;
            border-radius: 12px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            padding: 30px;
            overflow-x: auto;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            padding-bottom: 20px;
            border-bottom: 1px solid #eaeaea;
        }
        
        h1 {
            font-size: 2.5rem;
            color: #2c3e50;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .description {
            font-size: 1.1rem;
            color: #7f8c8d;
            max-width: 800px;
            margin: 0 auto;
        }
        
        .comparison-section {
            margin-bottom: 40px;
        }
        
        .section-title {
            font-size: 1.8rem;
            color: #3498db;
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #3498db;
            display: inline-block;
        }
        
        .audio-grid {
            display: grid;
            grid-template-columns: repeat(12, 1fr);
            gap: 15px;
            margin-bottom: 30px;
        }
        
        .audio-item {
            background: #f8f9fa;
            border-radius: 8px;
            padding: 15px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
            transition: transform 0.2s, box-shadow 0.2s;
        }
        
        .audio-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
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
            height: 40px;
            margin-bottom: 10px;
        }
        
        .video-container {
            width: 100%;
            height: 120px;
            border-radius: 6px;
            overflow: hidden;
            background: #000;
            margin-bottom: 10px;
        }
        
        video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .play-all-btn {
            display: block;
            margin: 20px auto;
            padding: 12px 25px;
            background: #3498db;
            color: white;
            border: none;
            border-radius: 6px;
            font-weight: 600;
            cursor: pointer;
            transition: background 0.3s;
            font-size: 1rem;
        }
        
        .play-all-btn:hover {
            background: #2980b9;
        }
        
        .footer-note {
            text-align: center;
            margin-top: 40px;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 1600px) {
            .audio-grid {
                grid-template-columns: repeat(6, 1fr);
            }
            
            .container {
                padding: 20px;
            }
        }
        
        @media (max-width: 1024px) {
            .audio-grid {
                grid-template-columns: repeat(4, 1fr);
            }
        }
        
        @media (max-width: 768px) {
            .audio-grid {
                grid-template-columns: repeat(2, 1fr);
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .section-title {
                font-size: 1.5rem;
            }
        }
        
        @media (max-width: 480px) {
            .audio-grid {
                grid-template-columns: 1fr;
            }
            
            body {
                padding: 10px;
            }
        }
    </style>
</head>
<body>
    <div id="app" class="container">
        <header>
            <h1>Audio Samples Comparison</h1>
            <p class="description">Compare different models and their outputs. Each row contains 12 samples for direct comparison.</p>
        </header>
        
        <main>
            <!-- First Comparison Group -->
            <section class="comparison-section">
                <h2 class="section-title">Comparison Group 1</h2>
                <div class="audio-grid">
                    <!-- Mixture -->
                    <div class="audio-item">
                        <h3 class="audio-title">Mixture</h3>
                        <audio controls>
                            <source src="/path/to/mixture1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- GT -->
                    <div class="audio-item">
                        <h3 class="audio-title">GT</h3>
                        <audio controls>
                            <source src="/path/to/gt1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Audio Cue -->
                    <div class="audio-item">
                        <h3 class="audio-title">Audio Cue</h3>
                        <audio controls>
                            <source src="/path/to/audio_cue1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Visual Cue -->
                    <div class="audio-item">
                        <h3 class="audio-title">Visual Cue</h3>
                        <div class="video-container">
                            <video controls>
                                <source src="/path/to/visual_cue1.mp4" type="video/mp4">
                            </video>
                        </div>
                    </div>
                    
                    <!-- Model 1 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 1</h3>
                        <audio controls>
                            <source src="/path/to/model1_1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 2 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 2</h3>
                        <audio controls>
                            <source src="/path/to/model2_1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 3 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 3</h3>
                        <audio controls>
                            <source src="/path/to/model3_1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 4 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 4</h3>
                        <audio controls>
                            <source src="/path/to/model4_1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 5 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 5</h3>
                        <audio controls>
                            <source src="/path/to/model5_1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 6 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 6</h3>
                        <audio controls>
                            <source src="/path/to/model6_1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 7 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 7</h3>
                        <audio controls>
                            <source src="/path/to/model7_1.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 8 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 8</h3>
                        <audio controls>
                            <source src="/path/to/model8_1.wav" type="audio/wav">
                        </audio>
                    </div>
                </div>
                
                <button class="play-all-btn" @click="playAllGroup(1)">Play All in Group 1</button>
            </section>
            
            <!-- Second Comparison Group -->
            <section class="comparison-section">
                <h2 class="section-title">Comparison Group 2</h2>
                <div class="audio-grid">
                    <!-- Mixture -->
                    <div class="audio-item">
                        <h3 class="audio-title">Mixture</h3>
                        <audio controls>
                            <source src="/path/to/mixture2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- GT -->
                    <div class="audio-item">
                        <h3 class="audio-title">GT</h3>
                        <audio controls>
                            <source src="/path/to/gt2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Audio Cue -->
                    <div class="audio-item">
                        <h3 class="audio-title">Audio Cue</h3>
                        <audio controls>
                            <source src="/path/to/audio_cue2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Visual Cue -->
                    <div class="audio-item">
                        <h3 class="audio-title">Visual Cue</h3>
                        <div class="video-container">
                            <video controls>
                                <source src="/path/to/visual_cue2.mp4" type="video/mp4">
                            </video>
                        </div>
                    </div>
                    
                    <!-- Model 1 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 1</h3>
                        <audio controls>
                            <source src="/path/to/model1_2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 2 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 2</h3>
                        <audio controls>
                            <source src="/path/to/model2_2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 3 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 3</h3>
                        <audio controls>
                            <source src="/path/to/model3_2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 4 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 4</h3>
                        <audio controls>
                            <source src="/path/to/model4_2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 5 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 5</h3>
                        <audio controls>
                            <source src="/path/to/model5_2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 6 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 6</h3>
                        <audio controls>
                            <source src="/path/to/model6_2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 7 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 7</h3>
                        <audio controls>
                            <source src="/path/to/model7_2.wav" type="audio/wav">
                        </audio>
                    </div>
                    
                    <!-- Model 8 -->
                    <div class="audio-item">
                        <h3 class="audio-title">Model 8</h3>
                        <audio controls>
                            <source src="/path/to/model8_2.wav" type="audio/wav">
                        </audio>
                    </div>
                </div>
                
                <button class="play-all-btn" @click="playAllGroup(2)">Play All in Group 2</button>
            </section>
        </main>
        
        <footer class="footer-note">
            <p>Note: Replace the sample paths with your actual audio and video file paths.</p>
        </footer>
    </div>

    <script>
        const { createApp, ref } = Vue;
        
        createApp({
            setup() {
                // Function to play all audio in a group (simplified)
                const playAllGroup = (groupNum) => {
                    const audioElements = document.querySelectorAll(`.comparison-section:nth-child(${groupNum + 1}) audio`);
                    audioElements.forEach(audio => {
                        audio.play().catch(e => console.log("Autoplay prevented:", e));
                    });
                    
                    alert(`Playing all audio samples in Group ${groupNum}. Note: Due to browser autoplay policies, you may need to interact with each audio element manually.`);
                };
                
                return {
                    playAllGroup
                };
            }
        }).mount('#app');
    </script>
</body>
</html>
