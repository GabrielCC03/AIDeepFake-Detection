# AIDeepFake-Detection
implementing a CNN to classify images of campus environments as real or AI-generated.

# Binary Classification of Campus Images Using CNN

## Project Overview
This project implements a Convolutional Neural Network (CNN) to perform binary classification, distinguishing between real campus images and AI-generated campus images. It specifically focuses on images of the PolyU campus.

## Dataset
The dataset comprises two categories:
- **Real Campus Images:** Captured through video frames at different times, angles, and lighting conditions. Faces were blurred for privacy.
- **AI-Generated Images (aiart):** Created using multiple AI image-generation tools.

### Dataset Composition
- **Original Dataset:** 34 images (17 real, 17 aiart).
![Original Dataset](https://github.com/user-attachments/assets/6a685696-7fb7-4bae-b5e1-d97496c5278f)
- **Extended Dataset (after augmentation):** 
  - Training Data: 2062 samples (893 aiart, 1169 real).
  - Testing Data: 166 samples.
 ![Extended Dataset](https://github.com/user-attachments/assets/fca4f6a2-6e27-471e-b6eb-5aa908d33c5a)


### Data Augmentation Techniques
Data augmentation was employed to enhance the dataset's diversity and balance, applying transformations such as rotation, zooming, shearing, flipping, normalization, and brightness adjustment.
![Augmented](https://github.com/user-attachments/assets/0b3fa597-465e-458e-9d17-40163ea8ba7d)


## CNN Architecture
The sequential CNN architecture was developed using Keras, featuring:
![Architecture](https://github.com/user-attachments/assets/eae7b589-56ab-4aba-be4d-e4d5fd9f3a4f)

- **Convolutional Layers:** Feature extraction from images.
- **Pooling Layers:** Reduce spatial dimensions of data.
- **Dropout Layers:** Prevent overfitting by randomly dropping neurons.
- **Flatten Layer:** Converts multi-dimensional data to a 1D vector.
- **Fully Connected Layers (Dense):** Facilitate binary classification (real vs. aiart).

## Training and Validation
![Training Graph](https://github.com/user-attachments/assets/1241f70b-c336-4e71-906d-f8f8777777ee)


## Results
The best-performing CNN model achieved a **validation accuracy of 93.6%**. Models were further refined to ensure robustness and mitigate overfitting through careful tuning of epochs, learning rates, and dropout layers.
