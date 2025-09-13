# Call Quality Analyzer

## Overview
**Call Quality Analyzer** is a Python + Colab project that downloads, preprocesses, and analyzes sales calls from YouTube.  
It uses **Whisper (faster-whisper)** for transcription and **speaker diarization** to separate **Sales** and **Customer** segments.  
The system provides **talk-time ratio, question count, sentiment analysis, and actionable insights** in a single report.  

## ✨ Features  
- **YouTube Audio Download** – Fetches audio directly from YouTube using `yt-dlp`.  
- **Audio Preprocessing** – Normalizes and cleans audio for better transcription.  
- **Speaker Diarization** – Automatically labels speakers (Sales vs Customer).  
- **Transcription** – Fast and accurate transcription with `faster-whisper`.  
- **Conversation Analysis**  
  - ⏱ **Talk-Time Ratio** (who spoke how much)  
  - ❓ **Questions Count** (how engaging was the sales rep)  
  - 🗨 **Longest Monologue** (dominance in conversation)  
  - 😊 **Sentiment Analysis** (overall tone of call)  
- **Waveform Visualization** – See **before and after** processing audio.  
- **Audio Playback** – Listen to raw and processed audio directly in Colab.  

<br/>

## 🧠 Approach  
Our approach involves:  
1. **Audio Extraction** → Download YouTube audio using `yt-dlp`.  
2. **Preprocessing** → Normalize and save processed audio for better quality.  
3. **Speaker Diarization** → Separate Customer and Sales segments.  
4. **Transcription** → Convert speech to text using `faster-whisper`.  
5. **Analysis** → Calculate talk ratio, question count, sentiment, and insights.  
6. **Visualization & Playback** → Display waveform plots and playable audio.   

<br/>

## 🛠️ Technology Stack  
- **Programming Language**: Python  
- **Libraries Used**:  
  - Audio: `yt-dlp`, `librosa`, `soundfile`
  - Transcription: `faster-whisper`
  - Speaker Diarization: `pyannote.audio`
  - Visualization: `matplotlib`
  - NLP: `transformers` (sentiment analysis) 

<br/>

## 📊 Sample Output  
### Talk-Time Ratio  
![talk-time-ratio](![waveform](Images\speakers_timeline.png)  )  

### Waveform Comparison  
![waveform](Images\original_audio_waveform.png)  
![waveform](Images\processed_audio_waveform.png)  

### Call Sentiment
![call-sentiment](Images\call_sentiment.png)
<br/>

## Project Structure
```
Call-Quality-Analyzer/
│
├── call_quality_analyzer.ipynb    # Main Jupyter Notebook for analysis
├── README.md                      # Project documentation
├── Images/                        # Screenshots and images
│   ├── audio_compare.png
│   ├── call_sentiment.png
│   ├── most_freuent_words.png
│   ├── original_audio_waveform.png
│   ├── processed_audio_waveform.png
│   ├── speakers_timeline.png
│   └── Screenshot 2025-09-13 225608.png
```

## How to Run
1. Open `call_quality_analyzer.ipynb` in Google Colab.
2. Install required dependencies.
3. Run all cells step by step.
4. Provide a YouTube link to analyze the sales call.

<br/>

## 📌 Example YouTube Link
youtube_url = "https://www.youtube.com/watch?v=4ostqJD3Psc"


