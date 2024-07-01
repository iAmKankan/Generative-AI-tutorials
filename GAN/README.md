### ⬛ What is a Generative Adversarial Network?
**Generative Adversarial Networks (GANs)** are a powerful class of **neural networks** that are used for an **unsupervised learning**. **GANs** are made up of **two** neural networks, **a discriminator** and **a generator**. They use <ins><b>adversarial training to produce artificial data that is identical to actual data</ins></b>.

* The **Generator** attempts to <ins><b>fool</ins></b> the **Discriminator**, which is tasked with <ins>accurately distinguishing between produced and genuine data</ins>, by producing <ins><b>random noise samples</ins></b>.
* **Realistic**, **high-quality samples** are produced as a result of this competitive interaction, which drives both networks toward advancement.
* **GANs** are proving to be highly versatile artificial intelligence tools, as evidenced by their extensive use in **image synthesis**, **style transfer**, and **text-to-image synthesis**.
* They have also revolutionized generative modeling.

Through adversarial training, these models engage in a competitive interplay until the generator becomes adept at creating realistic samples, fooling the discriminator approximately half the time.

Generative Adversarial Networks (GANs) can be broken down into three parts:
* <ins><b>Generative:</ins></b> To learn a generative model, which describes how data is generated in terms of a probabilistic model.
* <ins><b>Adversarial:</ins></b> The word adversarial refers to setting one thing up against another. This means that, in the context of GANs, the generative result is compared with the actual images in the data set. A mechanism known as a discriminator is used to apply a model that attempts to distinguish between real and fake images.
* <ins><b>Networks:</ins></b> Use deep neural networks as artificial intelligence (AI) algorithms for training purposes.


### 🔲 Types of GANs
1. <ins><b>Vanilla GAN:</ins></b> This is the simplest type of **GAN**. Here, the **Generator** and the **Discriminator** are simple a basic **multi-layer perceptrons**. In **vanilla GAN**, the algorithm is really simple, it tries to **optimize** the **mathematical equation** using **stochastic gradient descent**.
2. <ins><b>Conditional GAN (CGAN):</ins></b> **CGAN** can be described as a deep learning method in which some conditional parameters are put into place.
    * In **CGAN**, an additional parameter **‘y’** is added to the **Generator** for generating the corresponding data.
    * Labels are also put into the input to the **Discriminator** in order for the **Discriminator** to help distinguish the **real data** from the **fake generated data**.
3. <ins><b>Deep Convolutional GAN (DCGAN):</ins></b> **DCGAN** is one of the most popular and also the most successful implementations of **GAN**. It is composed of **ConvNets** in place of **multi-layer perceptrons**.
   * The **ConvNets** are implemented without **max pooling**, which is in fact replaced by **convolutional stride**.
   * Also, the layers are **not fully connected**.
4. <ins><b>Laplacian Pyramid GAN (LAPGAN):</ins></b> The **Laplacian pyramid** is a **linear invertible image representation** consisting of a set of band-pass images, spaced an octave apart, plus a low-frequency residual.
   * This approach uses multiple numbers of **Generator** and **Discriminator** networks and different levels of the **Laplacian Pyramid**.
   * This approach is mainly used because it produces very **high-quality images**. The image is **down-sampled** at first at each layer of the **pyramid** and then it is again up-scaled at each layer in a **backward pass** where the image acquires some noise from the **Conditional GAN** at these layers until it reaches its original size.
5. <ins><b>Super Resolution GAN (SRGAN):</ins></b> **SRGAN** as the name suggests is a way of designing a GAN in which a deep neural network is used along with an **adversarial network** in order to produce **higher-resolution images**. This type of **GAN** is particularly useful in optimally up-scaling native low-resolution images to enhance their details minimizing errors while doing so.

### 🔲 Architecture of GANs
A Generative Adversarial Network (GAN) is composed of two primary parts, which are the Generator and the Discriminator.

### <ins>Generator Model</ins>
A key element responsible for creating fresh, accurate data in a Generative Adversarial Network (GAN) is the generator model. The generator takes random noise as input and converts it into complex data samples, such text or images. It is commonly depicted as a deep neural network.

The training data’s underlying distribution is captured by layers of learnable parameters in its design through training. The generator adjusts its output to produce samples that closely mimic real data as it is being trained by using backpropagation to fine-tune its parameters.

The generator’s ability to generate high-quality, varied samples that can fool the discriminator is what makes it successful.

#### Generator Loss
The objective of the generator in a GAN is to produce synthetic samples that are realistic enough to fool the discriminator. The generator achieves this by minimizing its loss function $\large{\color{Purple}J_G}$​. The loss is minimized when the log probability is maximized, i.e., when the discriminator is highly likely to classify the generated samples as real. The following equation is given below:

$$\Large{\color{Purple}J_G =\dfrac{1}{m}\sum_{i=1}^{m} \log D(G(z_i))}$$​

#### Where
* $\large{\color{Purple}J_G}$ measure how well the generator is fooling the discriminator.
* $\large{\color{Purple}\log D(G(z_i))}$ represents log probability of the discriminator being correct for generated samples.
* The generator aims to minimize this loss, encouraging the production of samples that the discriminator classifies as real $\large{\color{Purple}(\log D(G(z_i)))}$ , close to 1

### <ins>Discriminator Model</ins>
An artificial neural network called a discriminator model is used in Generative Adversarial Networks (GANs) to differentiate between generated and actual input. By evaluating input samples and allocating probability of authenticity, the discriminator functions as a binary classifier.

Over time, the discriminator learns to differentiate between genuine data from the dataset and artificial samples created by the generator. This allows it to progressively hone its parameters and increase its level of proficiency.

Convolutional layers or pertinent structures for other modalities are usually used in its architecture when dealing with picture data. Maximizing the discriminator’s capacity to accurately identify generated samples as fraudulent and real samples as authentic is the aim of the adversarial training procedure. The discriminator grows increasingly discriminating as a result of the generator and discriminator’s interaction, which helps the GAN produce extremely realistic-looking synthetic data overall.

#### Discriminator Loss
The discriminator reduces the negative log likelihood of correctly classifying both produced and real samples. This loss incentivizes the discriminator to accurately categorize generated samples as fake and real samples with the following equation:

$$\Large{\color{Purple}J_G =\dfrac{1}{m}\sum_{i=1}^{m}  \log D(x_i) - \dfrac{1}{m}\sum_{i=1}^{m} \log (1-D(G(z_i)))}$$​


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
