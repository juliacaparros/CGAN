# CGAN
In this first part, you are asked to train and test a CGAN for the generation of fake handwritten digits (and letters).

Let's just recall what training a model means in machine learning. It is in fact quite simple: given a model architecture, use an optimization scheme to minimize a loss function (representing the gap between the data and the model predictions) in order to find the optimal values of the model parameters. In this Section, all of these elements are treated one by one.

Let's maybe first recall the global architecture of the a GAN model. GANs are deep neural networks composed of two parts: a generator and a discriminator. Those two parts are trained as opponents (hence "adversarial"). On one side, the generator tries, from random latent vectors, to create new fake data that can fool the discriminator into thinking they are really coming from the dataset. Meanwhile, the discriminator tries to distinguish between true and fake data.

Conditional GAN (CGAN), introduced in 2014 by Mirza and Osindero, is a variation of the classical GAN architecture that aims to give control the generated outputs by inputting (in addition to the latent vector) a label corresponding to what should be generated. In particular, the generator and the discriminator both receive the label, i.e. the class, that should be generated or discriminated. During inference, this label can be chosen by the user, similar to prompts for LLMs like ChatGPT. The figure below illustrates the structural difference between GAN and CGAN.
