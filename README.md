# Common Representation Learning using Step-based Correlation Multi-Modal CNN

Implementation of the paper *[Common Representation Learning Using Step-based Correlation Multi-Modal CNN](https://arxiv.org/pdf/1711.00003.pdf)* using both Keras and Pytorch.

# Aim
To make a novel step-based correlation multi-modal CNN(CorrMCNN) which reconstructs one view of the data given the other while increasing the interaction between the representations at each hidden layer or every intermediate step.

# Dataset

- MNIST handwritten digits dataset -60,000 images for training and 10,000 for testing.
-  Each image is split vertically into two halves so as to obtain an image of 28 x 14 = 392 features

# Technique: Deep Autoencoder based Approach
Multi-Modal Autoencoder is used which is two channeled AE that performs 2 types of reconstructions which provide the ability to adapt towards transfer learning tasks:
- Self-reconstruction of view from itself.
- Cross-reconstruction where one view is reconstructed given the other.

# Implementation
This research paper is an improvement over the *[Correlational Neural Networks](https://arxiv.org/pdf/1504.07225.pdf)* paper with the following additions:
- Introduced convolution layer in the encoding phase and deconvolution layer in the decoding stage of the Correlation multi-modalCNN(CorrMCNN)
- Batch Normalization in the intermediate layers
- Instead of using final hidden representations in the correlation loss, correlation is computed at each intermediate layer.

# Architecture

# Goals
- Minimize the self-reconstruction error.
- Minimize the cross-reconstruction error at each intermediate step.
- Maximize the correlation between the hidden representation of both views at each encoding step.


