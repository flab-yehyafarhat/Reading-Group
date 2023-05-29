
# Privacy & fairness related papers




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

# Can Copyright be Reduced to Privacy?
There is an increasing concern that generative AI models may produce outputs that are
remarkably similar to the copyrighted input content on which they are trained. This worry has
escalated as the quality and complexity of generative models have immensely improved, and
the availability of large datasets containing copyrighted material has increased. Researchers
are actively exploring strategies to mitigate the risk of producing infringing samples, and a
recent line of work suggests to employ techniques such as differential privacy and other forms
of algorithmic stability to safeguard copyrighted content.
In this work, we examine the question whether algorithmic stability techniques such as
differential privacy are suitable to ensure the responsible use of generative models without inadvertently violating copyright laws. We argue that there are fundamental differences between
privacy and copyright that should not be overlooked. In particular we highlight that although
algorithmic stability may be perceived as a practical tool to detect copying, it does not necessarily equate to copyright protection. Therefore, if it is adopted as standard for copyright
infringement, it may undermine copyright law intended purposes.

# Flocks of Stochastic Parrots: Differentially Private Prompt Learning for Large Language Models

Large language models (LLMs) are excellent in-context learners. However, the
sensitivity of data contained in prompts raises privacy concerns. Our work first
shows that these concerns are valid: we instantiate a simple but highly effective
membership inference attack against the data used to prompt LLMs. To address
this vulnerability, one could forego prompting and resort to fine-tuning LLMs with
known algorithms for private gradient descent. However, this comes at the expense
of the practicality and efficiency offered by prompting. Therefore, we propose
to privately learn to prompt. We first show that soft prompts can be obtained
privately through gradient descent on downstream data. However, this is not the
case for discrete prompts. Thus, we orchestrate a noisy vote among an ensemble of
LLMs presented with different prompts, i.e., a flock of stochastic parrots. The vote
privately transfers the flock’s knowledge into a single public prompt. We show that
LLMs prompted with our private algorithms closely match the non-private baselines.
For example, using GPT3 as the base model, we achieve a downstream accuracy
of 92.7% on the sst2 dataset with (ε = 0.147, δ = 10−6
)-differential privacy vs.
95.2% for the non-private baseline. Through our experiments, we also show that
our prompt-based approach is easily deployed with existing commercial APIs.

# Learning with Impartiality to Walk on the Pareto Frontier of Fairness, Privacy, and Utility
Deploying machine learning (ML) models often requires both fairness and privacy guarantees. Both of these objectives present unique
trade-offs with the utility (e.g., accuracy) of the model. However, the mutual interactions between fairness, privacy, and utility are
less well-understood. As a result, often only one objective is optimized, while the others are tuned as hyper-parameters. Because
they implicitly prioritize certain objectives, such designs bias the model in pernicious, undetectable ways. To address this, we adopt
impartiality as a principle: design of ML pipelines should not favor one objective over another. We propose impartially-specified models,
which provide us with accurate Pareto frontiers that show the inherent trade-offs between the objectives. Extending two canonical
ML frameworks for privacy-preserving learning, we provide two methods (FairDP-SGD and FairPATE) to train impartially-specified
models and recover the Pareto frontier. Through theoretical privacy analysis and a comprehensive empirical study, we provide an
answer to the question of where fairness mitigation should be integrated within a privacy-aware ML pipeline.

# Differentially Private Attention Computation

Large language models (LLMs) have had a profound impact on numerous aspects of daily
life including natural language processing, content generation, research methodologies and so
on. However, one crucial issue concerning the inference results of large language models is
security and privacy. In many scenarios, the results generated by LLMs could possibly leak
many confidential or copyright information. A recent beautiful and breakthrough work [Vyas,
Kakade and Barak 2023] focus on such privacy issue of the LLMs from theoretical perspective.
It is well-known that computing the attention matrix is one of the major task during the LLMs
computation. Thus, how to give a provable privately guarantees of computing the attention
matrix is an important research direction.
Previous work [Alman and Song 2023, Brand, Song and Zhou 2023] have proposed provable
tight result for fast computation of attention without considering privacy concerns. One natural
mathematical formulation to quantity the privacy in theoretical computer science graduate
school textbook is differential privacy. Inspired by [Vyas, Kakade and Barak 2023], in this
work, we provide a provable result for showing how to differentially private approximate the
attention matrix.
From technique perspective, our result replies on a pioneering work in the area of differential
privacy by [Alabi, Kothari, Tankala, Venkat and Zhang 2022].

