# Human Activity Recognition from Wearable Sensors

This project investigates **Human Activity Recognition** using multivariate time-series data from wearable sensors. The study compares multiple modeling paradigms:

- Deep learning (LSTM),
- Classical neural networks,
- Frequency-domain approaches (FFT),
- Tree-based models (Random Forest, XGBoost),
- Symbolic time-series methods (WEASEL-MUSE).

The objective is to evaluate how different representations and learning strategies impact classification performance across human activities.

## Dataset

The dataset consists of multivariate accelerometer signals collected from 33 participants performing 9 activities.

Each sample includes:
- 6 sensor channels (wrist + thigh, three axes each),
- 100 Hz sampling rate (with variable activity length),
- numeric values in [-8, 8].

Activities include both **dynamic** (e.g. walking, jogging) and **static** (e.g. sitting, lying) assignments.



## Models

### Deep Learning

- **LSTM** – sequence modeling of temporal dependencies  
- **Feedforward NN** – baseline on flattened features  
- **FFT-based NN** – operates on spectral features  

### Classical ML

- **Random Forest**
- **XGBoost** 

### Symbolic ML

- **WEASEL-MUSE** (in Jupyter notebooks)

## Feature Representations

The project explores multiple representations of time-series data:

### 1. Time-Domain Signals
Raw sensor values used directly for learning.

### 2. Frequency-Domain (FFT)
Captures periodic patterns in motion signals.

### 3. Symbolic Representation (WEASEL-MUSE)
A dictionary-based approach for multivariate time-series classification, based on FFT.