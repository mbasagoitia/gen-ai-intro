# ChatGPT

## Pretraining vs Supervised Fine Tuning

In pretraining, we take large amounts of data from the internet, split them into sentences, and then separate sentences into two parts: the input x, and the output y, (masking parts of the sentences) which is a **ground truth.** The model will try to predict y and construct the original sentence. We can compare the true value y with the model's output y*, which we can use to calculate loss, then feed that back into the model to update/train it. Self-supervised learning.

Fine tuning involves taking a pretrained model and adding extra modifications from a smaller dataset so that it can perform specific tasks. Humans provide inputs and labeled outputs to the model, which will again predict y, calculate loss, and update the model. In this case, the ground truth is specific data that came from humans for a specialized purpose, rather than the internet. In this way, the model becomes good at prompt and response. Supervised learning.

## Reinforcement Learning with Human Feedback (RLHF)

Reinforcement learning came from the field of robotics and assumes there is an agent and an environment. The agent may have varying levels of information about the environment (perhaps the ChatGPT interface and its users) and makes observations (prompts) about the environment and then performs actions to change the environment (response). It may receive a reward from the environment that is used to update the parameters of the agent.

A reward predictor, which is trained by human feedback to derive the ground truth, predicts the reward (score) for the agent given the prompt and response pair.