# **Audio Classification Project Using Deep Learning**

A deep learning-based project to classify urban sounds into distinct categories using the UrbanSound8K dataset.

## Technologies Used

- **Python:** Programming language.
- **NumPy:** For numerical computations.
- **Pandas:** For handling dataset metadata.
- **Librosa:** For audio signal processing and feature extraction.
- **Matplotlib:** For visualizations.
- **TensorFlow/Keras:** For building and training the CNN model.

## **Dataset**

The dataset used in this project is [UrbanSound8K](https://urbansounddataset.weebly.com/urbansound8k.html), which contains 8,732 labeled sound excerpts (≤4 seconds) of urban sounds belonging to 10 classes:

- **air_conditioner**
- **car_horn**
- **children_playing**
- **dog_bark**
- **drilling**
- **engine_idling**
- **gun_shot**
- **jackhammer**
- **siren**
- **street_music**

### **Metadata File**: `UrbanSound8K.csv`

This file provides detailed information about each audio file in the dataset, including:

- **slice_file_name**: The audio file name in the format `[fsID]-[classID]-[occurrenceID]-[sliceID].wav`
  - **[fsID]**: Freesound ID of the recording.
  - **[classID]**: Numeric identifier of the sound class (e.g., 0 = air_conditioner).
  - **[occurrenceID]**: Distinguishes occurrences of the sound in the original recording.
  - **[sliceID]**: Distinguishes slices from the same occurrence.
- **fsID**: Freesound ID of the recording.
- **start / end**: Start and end time of the slice in the original recording.
- **salience**: A subjective rating of the sound’s prominence (1 = foreground, 2 = background).
- **fold**: Fold number (1–10) for cross-validation.
- **classID**: Numeric identifier of the sound class (e.g., 0 = air_conditioner).
- **class**: Human-readable class name (e.g., "air_conditioner").

## **Objective**

This study aims to classify urban sounds into the aforementioned categories using a **Convolutional Neural Network (CNN)** model.

## **Project Files**

1. **`preprocessing.ipynb`**

   - Performs preprocessing steps such as:
     - Audio file loading.
     - Feature extraction (e.g., Mel-spectrograms).
     - Dataset preparation for model training.

2. **`model_preparation_and_training.ipynb`**
   - Builds and trains a CNN model on the processed data.
   - Evaluates model performance using metrics such as loss and accuracy.

## **Results**

### **Top Three Training Results**:

| Model   | Loss   | Accuracy |
| ------- | ------ | -------- |
| Model 1 | 0.4307 | 86.87%   |
| Model 2 | 0.3629 | 89.27%   |
| Model 3 | 0.4355 | 88.01%   |

## **How to Use**

### **Step 1: Clone the Repository**

```bash
git clone https://github.com/your-username/audio-classification-project.git
cd audio-classification-project
```

### **Step 2: Install Dependencies**

Ensure you have Python and the necessary libraries installed. You can install the dependencies using:

```bash
pip install numpy pandas librosa matplotlib tensorflow keras
```

### **Step 3: Run Preprocessing**

Run the preprocessing.ipynb notebook to preprocess the dataset and extract features.

```bash
jupyter notebook preprocessing.ipynb
```

### **Step 4: Train the Model**

Run the model_preparation_and_training.ipynb notebook to train and evaluate the CNN model on the processed data.

```bash
jupyter notebook model_preparation_and_training.ipynb
```
