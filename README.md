# Series Sound

**Sonification of financial time series through spectral analysis and harmonic frequency mapping.**

This project transforms percentage changes in financial time series into audible frequencies using spectral decomposition and musical note quantization. It generates both a CSV file with the mapped notes and a WAV audio file for auditory structural analysis.

---

## Overview

Series Sound explores financial signal sonification by converting market dynamics into harmonic audio representations.

By combining spectral analysis, harmonic proportions, MIDI note approximation, and pure tone synthesis, this project enables auditory inspection of time series structure and volatility regimes.

---

## Features

- **Spectral Analysis** – Hann window and peak detection to extract the fundamental frequency  
- **Harmonic Mapping** – Just intonation proportions (unison, major third, perfect fifth, etc.)  
- **Dynamic Scaling** – Maps percentage changes to frequency variations  
- **MIDI Conversion** – Identifies the closest musical note for each frequency  
- **Audio Synthesis** – Pure sine wave generation  
- **Interactive Selection** – Choose from available `.parquet` files in the `X_syntetic` folder  

---

## Project Structure

series-sound/
│
├── Spectral_Analysis.py # Main script
├── requirements.txt # Python dependencies
├── LICENSE # MIT License
├── README.md
│
├── X_syntetic/ # Input folder with .parquet files (named by date)
│ └── YYYY-MM-DD.parquet
│
└── MUSIC/ # Output folder (created automatically)
├── output_YYYY-MM-DD.csv
└── audio_YYYY-MM-DD.wav


---

## Installation

### 1 Clone the repository

```bash
git clone https://github.com/newnes/series-sound.git
cd series-sound

### 2 Create and activate a virtual environment (recommended)
```bash
python -m venv venv

Windows
```bash
venv\Scripts\activate

macOS/Linux
```bash
source venv/bin/activate

### 3 Install dependencies
```bash
pip install -r requirements.txt




