### 
Generative adversarial networks (GANs) are an exciting recent innovation in machine learning. GANs are generative models: they create new data instances that resemble your training data. For example, GANs can create images that look like photographs of human faces, even though the faces don't belong to any real person. These images were created by a GAN: 

<p align="center">
  <img src="https://github.com/iAmKankan/Generative-AI-tutorials/assets/12748752/219d1fe4-cf24-436d-aff5-7db85c92b66f" width=50%/>
</p>

GANs achieve this level of realism by pairing a generator, which learns to produce the target output, with a discriminator, which learns to distinguish true data from the output of the generator. The generator tries to fool the discriminator, and the discriminator tries to keep from being fooled.

### Background: What is a Generative Model? 

What does "generative" mean in the name "Generative Adversarial Network"? "Generative" describes a class of statistical models that contrasts with discriminative models.

Informally:

Generative models can generate new data instances.
Discriminative models discriminate between different kinds of data instances.
A generative model could generate new photos of animals that look like real animals, while a discriminative model could tell a dog from a cat. GANs are just one kind of generative model.

More formally, given a set of data instances X and a set of labels Y:

Generative models capture the joint probability p(X, Y), or just p(X) if there are no labels.
Discriminative models capture the conditional probability p(Y | X).
A generative model includes the distribution of the data itself, and tells you how likely a given example is. For example, models that predict the next word in a sequence are typically generative models (usually much simpler than GANs) because they can assign a probability to a sequence of words.

A discriminative model ignores the question of whether a given instance is likely, and just tells you how likely a label is to apply to the instance.

Note that this is a very general definition. There are many kinds of generative model. GANs are just one kind of generative model.

Modeling Probabilities
Neither kind of model has to return a number representing a probability. You can model the distribution of data by imitating that distribution.

For example, a discriminative classifier like a decision tree can label an instance without assigning a probability to that label. Such a classifier would still be a model because the distribution of all predicted labels would model the real distribution of labels in the data.

Similarly, a generative model can model a distribution by producing convincing "fake" data that looks like it's drawn from that distribution.
