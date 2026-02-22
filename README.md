# Series Sound

**Sonification of financial time series through spectral analysis and musical note mapping.**

This project transforms percentage changes in financial time series into audible frequencies using harmonic proportions and fundamental frequency detection. It generates both a CSV file with the mapped notes and a WAV audio file for auditory analysis.

---

## Features

- **Spectral analysis** – Hann window and peak detection to extract the fundamental frequency.
- **Harmonic mapping** – Just intonation proportions (unison, major third, perfect fifth, etc.).
- **Dynamic scaling** – Maps percentage changes to frequency variations.
- **MIDI conversion** – Identifies the closest musical note for each frequency.
- **Audio synthesis** – Pure tones at the calculated frequencies.
- **Interactive date selection** – Choose from available `.parquet` files in the `X_syntetic` folder.

---

## Project Structure

series-sound/
├── Spectral_Analysis.py # Main script
├── requirements.txt # Python dependencies
├── LICENSE # MIT License
├── README.md # This file
├── X_syntetic/ # Input folder with .parquet files (named by date)
└── MUSIC/ # Output folder (created automatically)
├── output_YYYY-MM-DD.csv # Note mapping for each processed date
└── audio_YYYY-MM-DD.wav # Generated audio file

---

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/newnes/series-sound.git
   cd series-sound

2. **Create and activate a virtual environment (recommended)**
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt

---

## Usage

1. ** Prepare your data**

   Place your .parquet files inside the X_syntetic/ folder. Each file    must be named with a date, for example 2022-05-12.parquet, and    contain a column named value.

2. ** Run the script**
   ```bash
   python Spectral_Analysis.py

3. ** Select a date**
   The script will list all available dates. Enter the number    corresponding to the date you want to process, or press q to quit.

4. ** Get the outputs**
   A CSV file with the note mapping: MUSIC/output_<date>.csv
   A WAV audio file: MUSIC/audio_<date>.wav

## Example run

Available dates:
  1. 2022-05-12
  2. 2022-05-13
  3. 2022-05-14

Enter the number of the date you want to analyze (or 'q' to quit): 1

Processing date: 2022-05-12
Generating notes: 100%|██████████| 1440/1440 [00:02<00:00, 500.00it/s]
Generating audio: 100%|██████████| 1440/1440 [00:05<00:00, 250.00it/s]
✅ Audio generated: MUSIC/audio_2022-05-12.wav
✅ CSV saved: MUSIC/output_2022-05-12.csv

## Dependencies

All required packages are listed in requirements.txt:

numpy

pandas

librosa

soundfile

scipy

tqdm

Install them with:
   
   ```bash
   pip install -r requirements.txt

---

##  License

This project is licensed under the MIT License.
See the LICENSE file for details.

MIT License

Copyright (c) 2025 Nestor Mendez.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

## Contributing
Contributions, issues, and feature requests are welcome!
Feel free to open an issue or submit a pull request.

--- 

## Author
Nestor Mendez

GitHub: @newnes
