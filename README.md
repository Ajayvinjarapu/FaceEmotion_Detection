# Real-Time Emotion Detection System

## Project Overview
This system detects facial emotions (Happy, Sad, Neutral) in real-time using:
1. **Haar Cascade** for face detection
2. **HOG Features** for image representation
3. **SVM Classifier** for emotion prediction

## System Components
1. **Data Collection Script** (`In[1]`):
   - Captures facial images from webcam
   - Classifies into: Happy ('h'), Sad ('s'), Neutral ('n')
   - Saves to `dataset/{emotion}` folders
   - Press 'q' to quit

2. **Training Script** (`In[2]`):
   - Extracts HOG features (8×8 pixels/cell, 2×2 cells/block)
   - Uses Linear SVM classifier
   - Saves model as `emotion_svm_hog.pkl`

3. **Detection Script** (`In[4]`):
   - Real-time emotion prediction
   - Displays bounding box + emotion label
   - Press 'q' to exit

## Installation
```bash
pip install opencv-python scikit-learn scikit-image numpy joblib
```

## Usage
1.First run the data collection cell to build your dataset
2.Then execute the training cell to create the model
3.Finally run the detection cell for real-time prediction

## Technical Specifications
  - Input Size: 64×64 grayscale

## Feature Extraction:
  - HOG (Histogram of Oriented Gradients)
  - Parameters: 8×8 pixel cells, 2×2 cell blocks

## Classifier:
  - SVM with linear kernel
  - Probability estimates enabled

## Sample Outputs
![Screenshot 2025-04-18 005739](https://github.com/user-attachments/assets/46ed8d3a-b259-4950-a35e-d64b48078fd6)

![Screenshot 2025-04-18 010237](https://github.com/user-attachments/assets/77be9c5b-dfac-4500-939c-2f5cf34ee5a0)

![Screenshot 2025-04-18 010115](https://github.com/user-attachments/assets/03d76531-1c42-4209-aa5b-9b076edb2833)
