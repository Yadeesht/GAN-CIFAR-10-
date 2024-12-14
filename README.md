# GAN-CIFAR-10

This project showcases the implementation of a Generative Adversarial Network (GAN) designed to generate realistic images using the CIFAR-10 dataset. A GAN comprises two competing neural networks: the generator, which creates synthetic data, and the discriminator, which evaluates its authenticity. Together, they iteratively improve to produce image augmentation.

---

## Overview

### What is a GAN?

A Generative Adversarial Network (GAN) is a framework in deep learning involving two neural networks:

1. **Generator**: Produces fake data intended to resemble real data.
2. **Discriminator**: Differentiates between real data (from the dataset) and fake data (from the generator).

The two models are trained together in a process where the generator attempts to "fool" the discriminator, and the discriminator works to correctly classify data as real or fake. This adversarial setup results in increasingly realistic synthetic data.

### CIFAR-10 Dataset

The CIFAR-10 dataset consists of 60,000 32x32 color images across 10 distinct classes, with 6,000 images per class. These classes include:

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
---

## Model Details

### Generator

The generator takes random noise (a latent vector) as input and produces an image. Key components include:

- **Transposed convolution layers** for upsampling the latent vector.
- **Batch normalization** for stable training.
- **Leaky ReLU activations** to introduce non-linearities.
- **Upscalling** to interduce stability and understanding the global pattern

### Discriminator

The discriminator evaluates whether an input image is real or fake. Its architecture features:

- **Convolutional layers** for extracting image features.
- **Leaky ReLU activations** to address potential vanishing gradient issues.
- **Dropout layers** to prevent overfitting.

---
### Image Augumentation
The training process generates periodic outputs, showcasing the improvements in image quality. The evaluation of the model can be seen when the losses of both networks decrease. If the loss of one model reduces and the other spikes, this indicates an error in training, which helps refine the image augmentation.

---

## Results

The training process generates periodic outputs, showcasing the improvements in image quality.The evaluation of the model can be seen when the losses of both decreases. If the loss of one model reduces and other spikes this indicates the error in training.

---

## References

- **CIFAR-10 Dataset**: [Dataset Link](https://www.cs.toronto.edu/~kriz/cifar.html)

---

## Contributing

Contributions are welcome! Submit issues or pull requests to help improve the project.

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.


