# Probabilistic Image Models

## Autoregressive Image Model

Training: Unlike in a language model, we don't know the exact order of how a training image is drawn/created. No explicit underlying process. Masking: "guessing" how an image was drawn by guessing the last step (maybe the hat was the last added feature, maybe it was the nose, etc.). Diffusion masking: recursive levels of masking.

The model learns to reconstruct an image with intermediate steps that we constructed and comparing its generated value to the ground truth (original image) and calculating a loss function. Can also calculate gradient/loss for intermediate steps.

General form:
- In the diffusion/masking process, we want to know the distribution of the next "erasing" steps/what could be removed given previous versions closer to the original image. This is what we simulated:
p(y(t) | y(t-1), y(t-2)...y(0))
- In the generation step, we want to reverse the process and learn to "add back" steps. 
p(y(t-1) | y(t), y(t+1)...y(T)) <- y(T) is the first random stroke.

    - This expression models the probability distribution of the next signal to add to an image (or noise to remove), given all previous signals already added to the image. Note that y(T) is a random noise image.

## Denoising Diffusion Probabilistic Model (DDPM)

Became popular in 2020. Provides more variety, modes, diversity, and quality compared to GAN models.

The model wants to learn p(x(t-1) | x(t), t)

This expression models the probability distribution of the next signal to add to an image (or noise to remove), given only the previous signal, as well as the number of signals already added (or noises already removed), which is captured by t. 