# Call Quality Analyzer

## Overview
This project is a Call Quality Analyzer is a Python + Colab project that downloads, preprocesses, and analyzes sales calls from YouTube.  
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

## Project Structure
```
Call-Quality-Analyzer/
│
├── call_quality_analyzer.ipynb    # Main Jupyter Notebook for analysis
├── README.md                      # Project documentation
├── Images/                        # Screenshots and images
│   ├── Screenshot 2025-09-13 223354.png
│   ├── Screenshot 2025-09-13 223418.png
│   ├── Screenshot 2025-09-13 223434.png
│   ├── Screenshot 2025-09-13 224220.png
│   ├── Screenshot 2025-09-13 224234.png
│   ├── Screenshot 2025-09-13 224252.png
│   └── Screenshot 2025-09-13 225608.png
```

## 🚀 How to Run
1. **Open the notebook in Google Colab.**
2. **Install dependencies:**
3. **Run all cells step by step.**
4. **Provide your YouTube link to analyze the sales call.**

<br/>

## 📌 Example YouTube Link
youtube_url = "https://www.youtube.com/watch?v=4ostqJD3Psc"

## Requirements
- Python
- Jupyter Notebook
- Required libraries (install via pip or conda as specified in the notebook)
