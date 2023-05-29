
# Privacy & fairness related papers; respective titles and abstracts




# Differentially Private Latent Diffusion Models

Diffusion models (DMs) are widely used for generating high-quality image datasets.
However, since they operate directly in the high-dimensional pixel space, optimization of DMs is computationally expensive, requiring long training times. This
contributes to large amounts of noise being injected into the differentially private
learning process, due to the composability property of differential privacy. To
address this challenge, we propose training Latent Diffusion Models (LDMs) with
differential privacy. LDMs use powerful pre-trained autoencoders to reduce the
high-dimensional pixel space to a much lower-dimensional latent space, making
training DMs more efficient and fast. Unlike [Ghalebikesabi et al., 2023] that pretrains DMs with public data then fine-tunes them with private data, we fine-tune
only the attention modules of LDMs at varying layers with privacy-sensitive data,
reducing the number of trainable parameters by approximately 96% compared to
fine-tuning the entire DM. We test our algorithm on several public-private data
pairs, such as ImageNet as public data and CIFAR10 and CelebA as private data,
and SVHN as public data and MNIST as private data. Our approach provides a
promising direction for training more powerful, yet training-efficient differentially
private DMs that can produce high-quality synthetic images
