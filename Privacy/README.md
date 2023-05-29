
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


# Privacy Auditing with One (1) Training Run

We propose a scheme for auditing differentially private machine learning systems
with a single training run. This exploits the parallelism of being able to add or remove
multiple training examples independently. We analyze this using the connection between differential privacy and statistical generalization, which avoids the cost of group
privacy. Our auditing scheme requires minimal assumptions about the algorithm and
can be applied in the black-box or white-box setting

# Privacy Loss of Noisy Stochastic Gradient Descent Might Converge Even for Non-Convex Losses

The Noisy-SGD algorithm is widely used for privately training machine learning models. Traditional
privacy analyses of this algorithm assume that the internal state is publicly revealed, resulting in privacy
loss bounds that increase indefinitely with the number of iterations. However, recent findings have shown
that if the internal state remains hidden, then the privacy loss might remain bounded. Nevertheless, this
remarkable result heavily relies on the assumption of (strong) convexity of the loss function. It remains
an important open problem to further relax this condition while proving similar convergent upper bounds
on the privacy loss. In this work, we address this problem for DP-SGD, a popular variant of Noisy-SGD
that incorporates gradient clipping to limit the impact of individual samples on the training process. Our
findings demonstrate that the privacy loss of projected DP-SGD converges exponentially fast, without
requiring convexity or smoothness assumptions on the loss function. In addition, we analyze the privacy
loss of regularized (unprojected) DP-SGD. To obtain these results, we directly analyze the hockey-stick
divergence between coupled stochastic processes by relying on non-linear data processing inequalities.

