# 📞 Sales Call Analysis System  

## 📌 Overview  
The **Sales Call Analysis System** is a Python + Colab project that downloads, preprocesses, and analyzes sales calls from YouTube.  
It uses **Whisper (faster-whisper)** for transcription and **speaker diarization** to separate **Sales** and **Customer** segments.  
The system provides **talk-time ratio, question count, sentiment analysis, and actionable insights** in a single report.  

<br/>

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

This approach ensures **fast processing (<30 sec on Colab free tier)** and handles **poor audio quality** effectively.  

<br/>

## 🛠️ Technology Stack  
- **Programming Language**: Python  
- **Libraries Used**:  
  - `yt-dlp`, `librosa`, `soundfile` → Audio handling  
  - `faster-whisper` → Speech-to-text  
  - `pyannote.audio` → Speaker diarization  
  - `matplotlib` → Visualization  
  - `transformers` → Sentiment analysis  

<br/>

## 📊 Sample Output  
### Talk-Time Ratio  
![talk-time-ratio](photos/talk_time_ratio.png)  

### Waveform Comparison  
![waveform](photos/waveform_comparison.png)  

<br/>

## 📂 Project Structure  
```bash
Sales-Call-Analysis/
│
├── Sales_Call_Analysis.ipynb      # Main Colab Notebook
├── README.md                      # Project Documentation
├── photos/                        # Visualizations (waveforms, charts)
│   ├── talk_time_ratio.png
│   └── waveform_comparison.png
