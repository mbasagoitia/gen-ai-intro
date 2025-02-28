# Generative Adversarial Network

Uses a generator and discriminator

## Motivation for Studying

Can be used to generate images, music, text, videos, etc.

Interpolation: using images to generate new images

Modify attributes: learns underlying attributes from images to edit them in one attribute but not others (such as layout, lighting, etc.)

Image to image style transform: transforming elements of photos

## Loss Function

From the discriminator's perspective, the probability that real data should be inside of the decision boundary should be 1, and generated (fake) data should be 0. Data increasingly away from the decision boundary has a lower probability. Fake data inside the boundary counts as a discriminator loss, and real data outside of it also does (2 types of loss).

Conversely, the aim of the generator is to "fool" the discriminator, and the probability of generated data should aim to be 1. Generated data that falls outside of the decision boundary counts as a generator loss (1 type of loss). You can "count" magnitude of distance from the decision boundary to determine total loss. The generator doesn't consider real data when calculating loss.

## Calculating the Loss Function

The discriminator output for each data point is a function describing the probability that it is real.

D's prediction for the ith real data point: D(Xi)
D's prediction for the ith fake data point: D(G(Zi))

Discriminator loss: 1/m(summation of all i) log(1 - D(Xi)) + 1/m(summation of all i) log(D(G(Zi)))

Generator loss: 1/m(summation of all i) log(1 - D(G(Zi)))