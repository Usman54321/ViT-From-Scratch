# Vision Transformer in PyTorch

This project is an implementation of the Vision Transformer (ViT) model in PyTorch, following the [original paper](https://arxiv.org/abs/2010.11929) by Dosovitskiy et al. Vision Transformers are a novel approach to apply the powerful Transformer architecture to the domain of computer vision, achieving state-of-the-art results on various image recognition tasks.

## Model Overview

The Vision Transformer model consists of three main components:

* A patch embedding layer, which splits the input image into fixed-size patches and projects them into a high-dimensional embedding space.
* A Transformer encoder, which processes the sequence of patch embeddings and learns long-range dependencies between them. The encoder also outputs a special [CLS] token, which represents the global image representation.
* A classification head, which applies a linear layer on the [CLS] token and predicts the image label.

The model is trained end-to-end using standard cross-entropy loss.

## Dataset and Results

The dataset used for this project is the [MNIST dataset](https://en.wikipedia.org/wiki/MNIST_database), which is a collection of 70,000 grayscale images of handwritten digits from 0 to 9. The images are 28x28 pixels in size and are divided into 60,000 training images and 10,000 testing images.

The model is trained on a consumer-grade GPU for 10 epochs, with a batch size of 128 and a learning rate of 0.001. The model achieves 90% accuracy on the test set within 3 minutes of training, demonstrating the effectiveness and efficiency of the Vision Transformer model.
