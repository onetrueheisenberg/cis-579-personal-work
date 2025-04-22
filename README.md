# Speech Emotion Recognition & Music Recommendation #

This project aims to build an end-to-end Speech Emotion Recognition system that takes raw audio as input and classifies it into one of six emotional categories: happy, sad, neutral, fear, angry, and disgust. Based on the detected emotion, it then recommends suitable music using the Spotify API.

## Features ##

Preprocessing raw speech audio (silence trimming, padding)

Feature extraction using MFCCs, ZCR, RMS, and spectral features

Deep learning model with LSTM and CNN-LSTM architectures

Emotion classification accuracy of ~70%

Real-time emotion prediction on new audio samples

Spotify integration for emotion-based music recommendations

## Dataset Sources ##

CREMA-D

RAVDESS

TESS

SAVEE

Current version uses CREMA-D dataset mounted from Google Drive.

## Dependencies ##

Install the required packages:

pip install pydub spotipy librosa tensorflow scikit-learn matplotlib seaborn python-dotenv imbalanced-learn

## Pipeline Overview ##

1. Data Preparation

Load WAV files from emotion speech datasets

Parse metadata for gender and emotion labels

Merge data into a single DataFrame

2. Preprocessing

Silence trimming

Padding to a fixed duration

Resampling and uniform sample rate

3. Feature Extraction

Mel Frequency Cepstral Coefficients (MFCCs)

Zero Crossing Rate (ZCR)

Root Mean Square Energy (RMS)

Additional features: Spectral Centroid, Rolloff, Contrast, etc.

4. Model Building

LSTM-based sequence classifier

Optional: CNN-LSTM hybrid model with regularization

5. Training & Evaluation

Categorical Crossentropy Loss

Optimizers: RMSProp / Adam

Callbacks: EarlyStopping, ReduceLROnPlateau

Accuracy and Confusion Matrix evaluation

6. Emotion Prediction

Preprocess new audio samples

Predict emotion with trained model

Map emotion to musical genre

7. Spotify Music Recommendation

Uses spotipy and Spotify Developer API

Recommends top 5 tracks based on genre matching the emotion

## Example

### Example usage
predict_and_recommend("path/to/audio.wav", model, label_encoder, scaler)

🎧 Emotion-to-Genre Mapping

{
  'happy': 'pop',
  'sad': 'classical',
  'angry': 'rock',
  'fear': 'metal',
  'disgust': 'metal',
  'neutral': 'ambient'
}

## Notes

All models trained using Google Colab GPU backend

Audio preprocessing is critical for consistent performance

Dimensionality reduction and feature enhancement are key to improving accuracy

## API Keys

You must set your Spotify API credentials using:

SPOTIFY_CLIENT_ID = "your_client_id"
SPOTIFY_CLIENT_SECRET = "your_client_secret"

These can be created at Spotify Developer Dashboard.

## Future Improvements

Integrate visual modalities (e.g., facial expressions)

Use pretrained embeddings from Wav2Vec or Hubert

Improve real-time response with optimized model deployment

## Contributors

Shahina Rajamani
Shimil Shijo
Sundar Swaminathan


