<div align="center">

# ✍️ Handwritten Digit Recognition

### Convolutional Neural Network for MNIST classification

![python](https://img.shields.io/badge/Python-3.9+-3776AB?logo=python&logoColor=white)
![tensorflow](https://img.shields.io/badge/TensorFlow-FF6F00?logo=tensorflow&logoColor=white)
![keras](https://img.shields.io/badge/Keras-D00000?logo=keras&logoColor=white)
![last commit](https://img.shields.io/github/last-commit/virinchisai/Hand-Written-Digit-Recognition)
![stars](https://img.shields.io/github/stars/virinchisai/Hand-Written-Digit-Recognition?style=social)

</div>

A convolutional neural network trained on the **MNIST** dataset that recognizes
handwritten digits (0–9) with high accuracy. Implemented in Python with
TensorFlow/Keras as part of an undergraduate research project.

## 📰 Publication

This work was published as:

> **An Intelligent Way to Recognize Digits Using Convolutional Neural Networks**

## 🏗️ How it works

```mermaid
flowchart LR
    Input[Input Image<br/>28×28 grayscale]
    Conv1[Conv2D + ReLU]
    Pool1[MaxPooling]
    Conv2[Conv2D + ReLU]
    Pool2[MaxPooling]
    Flat[Flatten]
    Dense[Dense + Dropout]
    Output[Softmax<br/>10 classes]
    Input --> Conv1 --> Pool1 --> Conv2 --> Pool2 --> Flat --> Dense --> Output
```

## 🚀 Quick start

```bash
pip install tensorflow numpy matplotlib
python train.py        # train the model on MNIST
python predict.py img.png  # classify a digit image
```

## 📊 Approach

- Preprocessing: normalize pixels to [0, 1], reshape to (28, 28, 1)
- Architecture: two Conv2D + MaxPooling blocks → Flatten → Dense (128) → Dropout → Softmax (10)
- Loss: categorical cross-entropy. Optimizer: Adam.
- Evaluation: accuracy on the held-out MNIST test set

## 📜 License
MIT
