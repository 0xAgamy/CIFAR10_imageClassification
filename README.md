# CIFAR-10 Image Classification Project

This project demonstrates a deep learning model designed to classify images from the CIFAR-10 dataset. We start by implementing a simple convolutional neural network (CNN) prototype and progressively improve its performance by enhancing the data pipeline and model architecture.

---

## Project Overview
The goal of this project was to create and train a Convolutional Neural Network (CNN) to achieve high accuracy on the CIFAR-10 dataset. 

1. **Prototype Model**: Achieved ~60% accuracy on test data.
2. **Improved Model**: Achieved ~85% accuracy with a loss of 0.49 on test data.

---

## Dataset
The CIFAR-10 dataset consists of 60,000 color images (32x32 pixels) divided into 10 classes. The dataset is split into:
- Training data: 45,000 images
- Validation Data : 5,000 images
- Testing data: 10,000 images

---

## Model Development

### Prototype Model
1. **Preprocessing**:
   - Rescaled images to [0, 1].
   - Applied one-hot encoding to the labels.
   - Split data into training, validation, and testing sets.

2. **Architecture**:
   - Convolution + Pooling layers (3 blocks).
   - Fully connected (FC) layer followed by an output layer with 10 nodes (softmax activation).
   
3. **Results**:
   - **Accuracy**: ~60% on test data.

### Improved Model
1. **Preprocessing**:
   - Normalized the data.
   - Applied one-hot encoding to the labels.
   - Performed data augmentation (random flips, rotations, and shifts).

2. **Architecture** (inspired by VGGNet):
   - **Conv2D** layers with Batch Normalization and ReLU activation.
   - MaxPooling2D layers to reduce spatial dimensions.
   - Dropout layers for regularization.
   - Flattening followed by a Dense output layer with softmax activation.

 
---

## Training Details
- **Optimizer**: Adam
- **Learning Rate**: 0.0001
- **Batch Size**: 128
- **Epochs**: 125

---

## Evaluation and Results
- **Test Accuracy**: 85%
- **Test Loss**: 0.49

---
## Conclusion

- **Prototype Model**: Provided a basic framework for image classification (~60% accuracy).
- **Improved Model**: Achieved significant performance improvement (85% accuracy) through better preprocessing, data augmentation, and a VGGNet-inspired architecture.