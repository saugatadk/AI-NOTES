# Generative Adversarial Networks (GANs)

Generative modeling frames unsupervised distribution learning as a minimax two-player game between a Generator network ($G$) and a Discriminator network ($D$).

---

## 🧭 Chapter Modules

- **[Generative Adversarial Networks (gan.md)](gan.md)**:
  - Game-theoretic objective function and cross-entropy loss formulation.
  - Minimax optimization and Nash equilibrium dynamics.
  - Generator vs Discriminator alternating gradient update loops.

- **[Deep Convolutional GANs (dcgan.md)](dcgan.md)**:
  - Replacing fully connected layers with strided transposed convolutions.
  - Architectural constraints for training stability (Batch Normalization, LeakyReLU).
  - Generating high-resolution synthetic images from latent noise vectors.
