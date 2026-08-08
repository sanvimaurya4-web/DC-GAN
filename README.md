# DCGAN (Deep Convolutional Generative Adversarial Network)

An implementation of a Deep Convolutional Generative Adversarial Network (DCGAN) based on the paper [Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks](https://arxiv.org/abs/1511.06434) by Alec Radford, Luke Metz, and Soumith Chintala.

---

## 📌 Overview

DCGANs improve upon standard Generative Adversarial Networks (GANs) by using **Convolutional Neural Networks (CNNs)** instead of fully connected layers. This architecture brings spatial feature learning and structural hierarchy into the generative modeling process, resulting in significantly higher stability during training and better visual quality of generated images.

---

## 🏗️ Architecture & Key Features

* **Strided Convolutions in Discriminator:** Replaces spatial pooling (e.g., MaxPool) with strided convolutions to learn downsampling features.
* **Fractionally-strided (Transposed) Convolutions in Generator:** Used for spatial upsampling from noise vectors to high-resolution images.
* **Batch Normalization:** Applied across both the Generator and Discriminator to stabilize learning and mitigate mode collapse.
* **Activation Functions:**
  * **Generator:** `ReLU` activation for hidden layers and `Tanh` for the final output layer.
  * **Discriminator:** `LeakyReLU` activation across all layers to allow gradient flow.

---

## 🛠️ Project Structure

```text
├── data/               # Directory for dataset storage
├── models/             # Generator and Discriminator model architecture definitions
├── outputs/            # Saved generated samples and training loss plots
├── train.py            # Main training loop script
├── generate.py         # Inference script for generating new images
├── requirements.txt    # Project dependencies
└── README.md           # Project documentation
