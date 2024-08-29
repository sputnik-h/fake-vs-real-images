# AI vs. Real Image Classification: Shoe Authenticity Detection

This project aims to develop a Convolutional Neural Network (CNN) model to classify images of shoes as either AI-generated or real. As AI-generated images become more prevalent and increasingly indistinguishable from real images, distinguishing between them has critical implications for authenticity and trust in visual media, particularly in online resale platforms.

## Table of Contents
- [Introduction](#introduction)
- [Data Preparation](#data-preparation)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Contributors](#contributors)
- [Acknowledgments](#acknowledgments)

## Introduction

The project focuses on identifying the differences between real and AI-generated images of shoes, using a dataset containing 824 real and 1,357 AI-generated images. The real images were sourced from popular brands like Nike, Adidas, and Converse, while the AI-generated images were created using MidJourney, a generative AI tool. This classification has significant implications for maintaining trust on resale platforms by preventing the misuse of AI-generated images.

## Data Preparation

The dataset comprises 2,181 images, split into 824 real images and 1,357 AI-generated images. Images were resized to 240x240 pixels, and a train-test split was performed with 20% of the data reserved for testing. The AI-generated images include a wider variety of styles, such as boots and sandals, while the real images are primarily men's sneakers.

## Model Architecture

The CNN model consists of:
- A Conv2D layer with 3 filters, a 3x3 kernel, and ReLU activation.
- Pooling layers that reduce spatial dimensions by taking the max value within each window.
- A flatten layer that converts the 2D feature maps into a 1D vector.
- A fully connected (dense) layer with 64 neurons and ReLU activation.
- An output layer with a single neuron and sigmoid activation for binary classification.

The model was trained with a batch size of 200 and stopped early due to validation accuracy stabilization at 95.7%.

## Results

The model achieved:
- Training accuracy: 99.5%
- Validation accuracy: 95.7%
- Test accuracy: 93.8%

The model was able to generalize well, although it occasionally misclassified non-sneaker images as real, demonstrating the model's reliance on image style differences.

## Conclusion

The project provides a promising approach for detecting AI-generated images within a specific domain (shoes). Such models could benefit platforms like StockX by identifying potentially deceptive listings. Expanding the dataset to include more shoe styles would further improve the model’s robustness.

## Future Work

To improve model performance:
- Expand the dataset to include other shoe styles like boots, heels, and sandals.
- Refine the model to better handle stylistic variances in real images.

## Contributors

- **Tsubasa Lin** - Project code
- **Ethan Liu** - Project code
- **Jaden Mullin** - Project report
- **Joy Sun** - Project code
- **Justin Yang** - Project report

## Acknowledgments

Special thanks to Dr. Yingying Fan for guidance throughout this project.

---

This project is a part of the course "DSO 569 Deep Learning for Business Applications" at USC Marshall School of Business.
