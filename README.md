# cnn-cifar10-image-classification
# CIFAR-10 Image Classification using Convolutional Neural Networks (CNN)

## Overview

This project implements a Convolutional Neural Network (CNN) using TensorFlow/Keras to classify images from the CIFAR-10 dataset.

The model learns to classify images into one of 10 categories:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck
## Dataset
**CIFAR-10**

- 50,000 Training Images
- 10,000 Test Images
- 10 Classes
- Image Size: 32 × 32 × 3

Dataset Source:
https://www.cs.toronto.edu/~kriz/cifar.html

---

## Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Google Colab

## CNN Architecture

```text
Input Layer (32x32x3)

↓ Conv2D (32 filters)
↓ MaxPooling2D

↓ Conv2D (64 filters)
↓ MaxPooling2D

↓ Conv2D (128 filters)
↓ MaxPooling2D

↓ Flatten

↓ Dense (128 neurons)

↓ Dropout (0.5)

↓ Dense (10 neurons, Softmax)

## Model Summary

| Layer | Output Shape |
|---------|-------------|
| Conv2D | (30,30,32) |
| MaxPooling2D | (15,15,32) |
| Conv2D | (13,13,64) |
| MaxPooling2D | (6,6,64) |
| Conv2D | (4,4,128) |
| MaxPooling2D | (2,2,128) |
| Flatten | (512) |
| Dense | (128) |
| Dropout | (128) |
| Dense | (10) |

Total Parameters: **160,202**

## Training Configuration

| Parameter | Value |
|------------|---------|
| Optimizer | Adam |
| Loss Function | Sparse Categorical Crossentropy |
| Batch Size | 64 |
| Epochs | 15 |
| Activation | ReLU |
| Output Activation | Softmax |

---

## Results

### Final Performance

| Metric | Score |
|----------|---------|
| Training Accuracy | 79.8% |
| Test Accuracy | 72.55% |
| Test Loss | 0.838 |

---

## Learning Curves

### Accuracy Curve

The training and validation accuracy steadily improve throughout training.

![Accuracy Curve](accuracy_curve.png)

---

### Loss Curve

Training loss decreases consistently while validation loss stabilizes after several epochs.

![Loss Curve](loss_curve.png)

---

## Confusion Matrix

The confusion matrix illustrates class-wise prediction performance.

![Confusion Matrix](confusion_matrix.png)

---

## Key Observations

- Achieved over 72% test accuracy on CIFAR-10.
- Strong performance on:
  - Automobile
  - Ship
  - Truck
  - Horse

- Common misclassifications:
  - Cat ↔ Dog
  - Deer ↔ Horse
  - Bird ↔ Deer

- Slight overfitting observed after approximately 10 epochs.

---

## Project Structure

```text
cnn-cifar10-classifier/
│
├── CNN_CIFAR10_Project.ipynb
├── README.md
├── requirements.txt
│
├── accuracy_curve.png
├── loss_curve.png
├── confusion_matrix.png
│
└── cnn_cifar10_model.h5
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/cnn-cifar10-classifier.git
```

Move into the project directory:

```bash
cd cnn-cifar10-classifier
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## Run the Project

```bash
jupyter notebook
```

Open:

```text
CNN_CIFAR10_Project.ipynb
```

Run all cells sequentially.

---

## Future Improvements

- Data Augmentation
- Batch Normalization
- Transfer Learning (MobileNetV2, ResNet50)
- Hyperparameter Tuning
- Learning Rate Scheduling
- Model Deployment using Streamlit

---

## Author

Ganesh Kumar Reddy

Electronics and Communication Engineering (ECE)

Machine Learning & AI Enthusiast
