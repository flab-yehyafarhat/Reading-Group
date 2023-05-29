
# nonspecific ML focused papers 

# Neural Functional Transformers
The recent success of neural networks as implicit representation of data has driven
growing interest in neural functionals: models that can process other neural networks
as input by operating directly over their weight spaces. Nevertheless, constructing
expressive and efficient neural functional architectures that can handle
high-dimensional weight-space objects remains challenging. This paper uses the
attention mechanism to define a novel set of permutation equivariant weight-space
layers and composes them into deep equivariant models called neural functional
Transformers (NFTs). NFTs respect weight-space permutation symmetries while
incorporating the advantages of attention, which have exhibited remarkable success
across multiple domains. In experiments processing the weights of feedforward
MLPs and CNNs, we find that NFTs match or exceed the performance of prior
weight-space methods. We also leverage NFTs to develop INR2ARRAY, a novel
method for computing permutation invariant latent representations from the weights
of implicit neural representations (INRs). Our proposed method improves INR
classification accuracy by up to +17% over existing methods.

# Permutation Equivariant Neural Functionals
This work studies the design of neural networks that can process the weights or
gradients of other neural networks, which we refer to as neural functional networks
(NFNs). Despite a wide range of potential applications, including learned optimization,
processing implicit neural representations, network editing, and policy
evaluation, there are few unifying principles for designing effective architectures
that process the weights of other networks. We approach the design of neural
functionals through the lens of symmetry, in particular by focusing on the permutation
symmetries that arise in the weights of deep feedforward networks because
hidden layer neurons have no inherent order. We introduce a framework for building
permutation equivariant neural functionals, whose architectures encode these
symmetries as an inductive bias. The key building blocks of this framework are
NF-Layers (neural functional layers) that we constrain to be permutation equivariant
through an appropriate parameter sharing scheme. In our experiments, we
find that permutation equivariant neural functionals are effective on a diverse set of
tasks that require processing the weights of MLPs and CNNs, such as predicting
classifier generalization, producing “winning ticket” sparsity masks for initializations,
and editing the weights of implicit neural representations (INRs). In addition,
we provide code for our models and experiments.

# Visualizing the Loss Landscape of Neural Nets
Neural network training relies on our ability to find “good” minimizers of highly
non-convex loss functions. It is well-known that certain network architecture
designs (e.g., skip connections) produce loss functions that train easier, and wellchosen training parameters (batch size, learning rate, optimizer) produce minimizers that generalize better. However, the reasons for these differences, and their
effect on the underlying loss landscape, are not well understood. In this paper, we
explore the structure of neural loss functions, and the effect of loss landscapes on
generalization, using a range of visualization methods. First, we introduce a simple
“filter normalization” method that helps us visualize loss function curvature and
make meaningful side-by-side comparisons between loss functions. Then, using
a variety of visualizations, we explore how network architecture affects the loss
landscape, and how training parameters affect the shape of minimizers.

# On progressive sharpening, flat minima and generalisation
We present a new approach to understanding the relationship between loss curvature and generalisation in deep learning. Specifically, we use existing empirical analyses of the spectrum of deep network loss Hessians to ground an ansatz tying together the loss Hessian and the input-output Jacobian of a deep neural network. We then prove a series of theoretical results which quantify the degree to which the input-output Jacobian of a model approximates its Lipschitz norm over a data distribution, and deduce a novel generalisation bound in terms of the empirical Jacobian. We use our ansatz, together with our theoretical results, to give a new account of the recently observed progressive sharpening phenomenon, as well as the generalisation properties of flat minima. Experimental evidence is provided to validate our claims.

# Deep reinforcement learning from human preferences
For sophisticated reinforcement learning (RL) systems to interact usefully with
real-world environments, we need to communicate complex goals to these systems.
In this work, we explore goals defined in terms of (non-expert) human preferences
between pairs of trajectory segments. We show that this approach can effectively
solve complex RL tasks without access to the reward function, including Atari
games and simulated robot locomotion, while providing feedback on less than
1% of our agent’s interactions with the environment. This reduces the cost of
human oversight far enough that it can be practically applied to state-of-the-art
RL systems. To demonstrate the flexibility of our approach, we show that we can
successfully train complex novel behaviors with about an hour of human time.
These behaviors and environments are considerably more complex than any which
have been previously learned from human feedback.

# Backpropagation-free Training of Deep Physical Neural Networks

Recent years have witnessed the outstanding success of deep learning in various fields such as vision and natural language processing. This success is
largely indebted to the massive size of deep learning models that is expected to
increase unceasingly. This growth of the deep learning models is accompanied
by issues related to their considerable energy consumption, both during the
training and inference phases, as well as their scalability. Although a number
of work based on unconventional physical systems, such as wave-based frameworks, have been proposed which addresses the issue of energy efficiency in the
inference phase, efficient training of deep learning models has remained unaddressed. So far, training of digital deep learning models mainly relies on backpropagation, which is not suitable for physical implementation as it requires
perfect knowledge of the computation performed in the so called forward pass
of the neural network. Here, we tackle this issue by proposing a simple deep
neural network architecture augmented by a biologically plausible learning algorithm, referred to as ”model-free forward-forward training”. The proposed architecture enables training deep physical neural networks consisting
of layers of physical nonlinear systems, without requiring detailed knowledge
of the nonlinear physical layers’ properties. We show that our method outperforms state-of-the-art hardware-aware training methods by improving training speed, decreasing digital computations, and reducing power consumption
in physical systems, particularly optics. We demonstrate the robustness and
adaptability of the proposed method, even in systems exposed to dynamic or
unpredictable external perturbations. To showcase the universality of our approach, we train diverse wave-based physical neural networks that vary in the
underlying wave phenomenon and the type of non-linearity they use, to perform vowel and image classification tasks experimentally. This work paves the
way for the ambitious goals of hybrid training massive physical neural networks, which can offer high-speed and lower energy consumption not only for
inference but also during the training phase.

