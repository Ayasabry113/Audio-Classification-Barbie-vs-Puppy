# Audio Classification — Barbie vs Puppy

A supervised audio-classification project that distinguishes between Barbie and Puppy recordings using Librosa audio features and machine-learning classifiers.

## Dataset
The original notebook expects WAV recordings. The audio dataset was not included in the source notebook upload, so it must be supplied separately.

Create an `audio_data/` folder and place the WAV files inside it. Each filename must contain one of these class identifiers:
- `barbie` → label 0
- `puppy` → label 1

Example:
```text
audio_data/
├── barbie_001.wav
├── barbie_002.wav
├── puppy_001.wav
└── puppy_002.wav
```

## Features
- 13 MFCC means and 13 MFCC standard deviations
- Spectral centroid
- Spectral rolloff
- Zero-crossing rate

## Models
- Gaussian Naive Bayes implemented from scratch
- Logistic Regression
- Bagged Gaussian Naive Bayes
- Bagged Logistic Regression

## Evaluation
Accuracy, precision, recall, F1-score, classification report, and confusion matrix.

## Run
Install dependencies:
```bash
pip install -r requirements.txt
```
Open `Audio_Classification_Barbie_vs_Puppy.ipynb` in Jupyter or Google Colab. Update `DATA_DIR` to the location of your audio dataset, then run the notebook from top to bottom.

## Optional microphone recording
The notebook includes an optional local microphone recording example. It requires `sounddevice` and `scipy` and may not be supported in hosted notebook environments.

## Technologies
Python, Librosa, NumPy, Pandas, Matplotlib, and Scikit-learn.
