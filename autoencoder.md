# Autoencoder

An autoencoder is used to convert many dimensions of data into a smaller amount, usually the more important pieces of data that it learns to model. The decoder then decodes these dimensions to output the same number of dimensions as the input. With this data, we can calculate loss that occurred during this process. There may be intermediate steps/dimensions.

Example: image -> encode (downsample) -> code -> decode (upsample) -> image

**Latent** code, features, etc. refers to the internal part of the process, which are usually numbers that aren't intuitive to understand by people.

**Salient** features are things we can observe, see, hear, etc.

Making modifications, even small ones, in the latent space (code) can generate new data points in the data space (output). We can use random numbers to generate new, random outputs that we haven't seen before.

During **backpropagation**, the gradients of the loss are calculated and propagated back through the network.

For the discriminator, the loss function depends on the real and fake labels, and the gradients are computed accordingly, updating the discriminator's weights.

For the generator, the loss is computed based on how well it fooled the discriminator. The gradients for the generator's parameters are propagated back through the generator network.

Updating Weights:

The weights of both networks are updated through gradient descent (or some variant). The generator improves at producing more realistic images, and the discriminator improves at distinguishing between real and fake images.

These two networks are trained alternately, leading to an iterative process where the generator gets better at creating fake data, and the discriminator becomes more accurate at distinguishing fake from real data.