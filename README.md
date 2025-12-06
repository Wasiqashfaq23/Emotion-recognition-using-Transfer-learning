# Emotion Recognition with Deep Learning

This project performs facial emotion recognition using a MobileNetV2-based neural network.  
Two model versions are provided so people can directly compare results:

### Baseline Model (No Fine Tuning)
- Backbone frozen  
- Validation accuracy ≈ **37%**

### Fine-Tuned Model
- Last 30 MobileNetV2 layers unfrozen  
- Low learning rate for careful tuning  
- Validation accuracy ≈ **40%**

Both `.keras` model files are included in the repository.

---

## Features

- Real-time emotion detection using OpenCV and your webcam  
- Training code for both baseline and fine-tuned versions  
- Lightweight inference (runs even on a laptop with integrated graphics)  
- MobileNetV2 transfer learning with FER-style 48×48 grayscale images  

---

## Training Workflow (Google Colab)

Training was done on **Google Colab Free Tier**, using its GPU.  
The notebook includes:

- Dataset preprocessing  
- Creating the baseline MobileNetV2 model  
- Fine-tuning last 30 layers  
- Evaluating model performance  
- Saving `.keras` / `.h5` model files  

You can retrain your own version easily by opening the `.ipynb` file in Colab.

---

## Real-Time Emotion Detection

The real-time script loads the model and performs:

- Face detection (Haar Cascade)
- Emotion prediction (7 classes)
- Live webcam display with labels

To run it:

## Clone the repo:

git clone https://github.com/USERNAME/emotion-recognition.git
cd emotion-recognition

## Environment Setup (pyenv + Python 3.11.6)

This project was developed using **pyenv** with **Python 3.11.6**, because the latest Python did not support TensorFlow correctly.  
Using pyenv ensures a clean, isolated environment where all dependencies install without version conflicts.

### 1. Install pyenv
Follow installation instructions:  
https://github.com/pyenv/pyenv

### 2. Install Python 3.11.6 through pyenv
TensorFlow provides CPU wheels for Python 3.11, so installation works fine in a managed virtual environment.

## Install dependencies:

pip install -r requirements.txt

## Run real-time detection:

python realtime_emotion.py

## Libraries used

tensorflow==2.15.0
keras==2.15.0
opencv-python
numpy
matplotlib

