### ⬛ What is a Generative Adversarial Network?
**Generative Adversarial Networks (GANs)** are a powerful class of **neural networks** that are used for an **unsupervised learning**. GANs are made up of two neural networks, **a discriminator** and **a generator**. They use **adversarial training** to produce **artificial data** that is identical to actual data.

The Generator attempts to fool the Discriminator, which is tasked with accurately distinguishing between produced and genuine data, by producing random noise samples.
Realistic, high-quality samples are produced as a result of this competitive interaction, which drives both networks toward advancement.
GANs are proving to be highly versatile artificial intelligence tools, as evidenced by their extensive use in image synthesis, style transfer, and text-to-image synthesis.
They have also revolutionized generative modeling.
Through adversarial training, these models engage in a competitive interplay until the generator becomes adept at creating realistic samples, fooling the discriminator approximately half the time.

Generative Adversarial Networks (GANs) can be broken down into three parts:

Generative: To learn a generative model, which describes how data is generated in terms of a probabilistic model.
Adversarial: The word adversarial refers to setting one thing up against another. This means that, in the context of GANs, the generative result is compared with the actual images in the data set. A mechanism known as a discriminator is used to apply a model that attempts to distinguish between real and fake images.
Networks: Use deep neural networks as artificial intelligence (AI) algorithms for training purposes.








### ⬛ Generative adversarial networks (GANs)
**Generative adversarial networks (GANs)** are an exciting recent innovation in machine learning. **GANs** are **generative models**: they create **new data instances** that resemble your **training data**. For example, GANs can create **images** that look like photographs of human faces, even though the faces don't belong to any real person. 

<p align="center">
  <img src="https://github.com/iAmKankan/Generative-AI-tutorials/assets/12748752/219d1fe4-cf24-436d-aff5-7db85c92b66f" width=50%/>
  <br><ins><b><i>GAN produced human pictures</i></b></ins>
</p>

**GANs** achieve this level of realism by pairing a **generator**, which learns to produce the target output, with a **discriminator**, which learns to distinguish true data from the output of the generator. The **generator** tries to **fool** the **discriminator**, and the **discriminator** tries to keep from being **fooled**.

### 🔲 Background: What is a Generative Model? 

#### What does "generative" mean in the name "Generative Adversarial Network"?
$\Large Answer:$"Generative" describes a class of statistical models that contrasts with **discriminative** models.

#### Informally:
* **Generative** models can generate **new** **data instances**.
* **Discriminative** models discriminate between **different kinds** of **data instances**.

A **generative** model could generate new **photos of animals** that look like real animals, while a **discriminative** model could tell a **dog** from a **cat**. **GANs** are just one kind of **generative** model.

More formally, given a set of data instances $\large{\color{Purple}X}$ and a set of labels $\large{\color{Purple}Y}$:

* **Generative** models capture the joint probability $\large{\color{Purple}p(X, Y)}$ or just $\large{\color{Purple}p(X)}$ if there are no labels.
* **Discriminative** models capture the conditional probability $\large{\color{Purple}p(Y | X)}$.

A generative model includes the distribution of the data itself and tells you how likely a given example is. For example, models that predict the next word in a sequence are typically **generative** models (usually much simpler than **GANs**) because they can assign a **probability to a sequence of words**.

A **discriminative** model ignores the question of whether a given instance is likely and just tells you how likely a label is to apply to the instance.

Note that this is a very general definition. There are many kinds of generative model. GANs are just one kind of generative model.

### Modeling Probabilities
Neither kind of model has to return a number representing a probability. You can model the distribution of data by imitating that distribution.

For example, a discriminative classifier like a decision tree can label an instance without assigning a probability to that label. Such a classifier would still be a model because the distribution of all predicted labels would model the real distribution of labels in the data.

Similarly, a generative model can model a distribution by producing convincing "fake" data that looks like it's drawn from that distribution.

### ⬛ Resources
* [GeeksForGeeks](https://www.geeksforgeeks.org/generative-adversarial-network-gan/)
