
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

# Selective Pre-training for Private Fine-tuning

Suppose we want to train text prediction models in email clients or word processors. The models must preserve the
privacy of user data and adhere to a specific fixed size to meet memory and inference time requirements. We introduce
a generic framework to solve this problem. Specifically, we are given a public dataset Dpub and a private dataset Dpriv
corresponding to a downstream task T. How should we pre-train a fixed-size model M on Dpub and fine-tune it on
Dpriv such that performance of M with respect to T is maximized and M satisfies differential privacy with respect to
Dpriv? We show that pre-training on a subset of dataset Dpub that brings the public distribution closer to the private
distribution is a crucial ingredient to maximize the transfer learning abilities of M after pre-training, especially in the
regimes where model sizes are relatively small. Besides performance improvements, our framework also shows that
with careful pre-training and private fine-tuning, smaller models can match the performance of much larger models,
highlighting the promise of differentially private training as a tool for model compression and efficiency

# Personalized DP-SGD using Sampling Mechanisms

Personalized privacy becomes critical in deep learning for Trustworthy AI. While
Differentially Private Stochastic Gradient Descent (DP-SGD) is widely used in
deep learning methods supporting privacy, it provides the same level of privacy
to all individuals, which may lead to overprotection and low utility. In practice,
different users may require different privacy levels, and the model can be improved
by using more information about the users with lower privacy requirements. There
are also recent works on differential privacy of individuals when using DP-SGD,
but they are mostly about individual privacy accounting and do not focus on satisfying different privacy levels. We thus extend DP-SGD to support a recent privacy
notion called (Φ, ∆)-Personalized Differential Privacy ((Φ, ∆)-PDP), which extends an existing PDP concept called Φ-PDP. Our algorithm uses a multi-round
personalized sampling mechanism and embeds it within the DP-SGD iterations.
Experiments on real datasets show that our algorithm outperforms DP-SGD and
simple combinations of DP-SGD with existing PDP mechanisms in terms of model
performance and efficiency due to its embedded sampling mechanism.
