# Handwritten Digit Recognition using CNN

A Convolutional Neural Network (CNN) that recognizes handwritten digits (0-9), built with TensorFlow/Keras and trained on the MNIST dataset.

## Overview
The model is trained on 60,000 images and tested on 10,000 images of handwritten digits. It can also predict digits from your own custom image.

## Results
- **Test accuracy:** 98.88%
- **Test loss:** 0.0346
- **Training:** 5 epochs, reaching 99.41% training accuracy

## Model Architecture
| Layer | Details |
|-------|---------|
| Conv2D | 32 filters, 3x3, ReLU |
| MaxPooling2D | 2x2 |
| Conv2D | 64 filters, 3x3, ReLU |
| MaxPooling2D | 2x2 |
| Flatten | - |
| Dense | 64 units, ReLU |
| Dense (output) | 10 units, Softmax |

Total parameters: 121,930

## Tech Stack
Python, TensorFlow/Keras, NumPy, OpenCV, Matplotlib, Google Colab

## Steps
1. Load the MNIST dataset
2. Normalize pixel values (0-1) and reshape images to 28x28x1
3. Build the CNN
4. Compile with Adam optimizer and sparse categorical crossentropy loss
5. Train for 5 epochs and evaluate on test data
6. Predict digits from test images and from a custom handwritten image

## How to Run
1. Open `handwritten_digit_prediction_model.ipynb` in Google Colab
2. Run all cells (Runtime -> Run all)
3. To test your own digit, upload a digit image and change the filename in the OpenCV step (`digit5.png`)

## Sample Prediction
Custom handwritten image of "5" -> Predicted digit: 5
