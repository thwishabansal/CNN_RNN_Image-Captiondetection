# Image Generation and Captioning using CNN and RNN

This project focuses on generating captions for images using Convolutional Neural Networks (CNNs) for image analysis and Recurrent Neural Networks (RNNs), specifically Long Short-Term Memory (LSTM) networks, for sequence prediction.

## Introduction

In today’s world, a lot of our communication is through pictures. Computers, however, need intricate procedures to comprehend images in the same way that human brains do. Over the years, deep learning techniques have advanced, and with a large amount of data available, we can create models that can generate captions for photos. CNNs are designed for image analysis and excel in tasks like image classification. They assign importance to different aspects of an input image through learnable weights and biases, facilitating image differentiation. On the other hand, RNNs, especially LSTM networks, are good at understanding order dependence in sequence prediction tasks like speech recognition and machine translation.

## Background

For image captioning, effective encoding of visual information and decoding into natural language descriptions are crucial. This typically involves an encoder (CNN) for extracting meaningful features from the input image and a decoder (RNN) for producing textual descriptions based on these features. Architectures like ResNet50 and Xception have demonstrated exceptional performance in various computer vision tasks, including image classification and object detection.

## Methodology

The project uses two directories - an image directory with 8091 images and a pickle file with 25000 captions. Each image is mapped to multiple captions. The images are resized to meet the requisite dimensions, typically 224x224 pixels, which is important for compatibility with ResNet. The pre-trained ResNet50 model is used to extract features from the resized images. These extracted features are then matched with their corresponding captions by comparing filenames. Captions are tokenized and converted into sequences of integers, padded to achieve consistent length for LSTM input. Data is split into training and testing sets and converted into TensorFlow datasets.

## Model Evaluation

Two models are evaluated - one using ResNet and the other using Xception. Both models use LSTM layers for sequence prediction. The ResNet-based model achieves a loss of 1.7854 and an accuracy of 70.49% on the test data. The Xception-based model achieves a test loss of 1869.19 and a test accuracy of 71.47%. The models are evaluated on a sample image to generate captions.

## Conclusion

The project demonstrates the use of CNNs and RNNs, specifically LSTM networks, in image captioning. While the models show impressive accuracy rates, there is still room for improvement, especially in improving the quality of generated captions. Further research may involve investigating more complex structures and using bigger training datasets.

