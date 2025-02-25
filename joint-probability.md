# Joint Probability for Generative Models

Lots of possibilities, but which one is the most probable?

**Joint probability** is the probability of a set of events occurring together. An **event** occurs when a slot is filled with an item in the vocabulary.

We can calculate the **probability distribution** with the data frequency. Probability = frequency / total

## Probability value vs probability distribution

Probability distribution (of all possibilities) is given by p(x1) = [0.58, 0.42] <- these values must add up to 1 to be a valid probability distribution

Probability value of x1 = meow = 0.58
or x1 = woof = 0.58

## Sampling from a Joint Probability Distribution

Some creations/combinations are more probable than others. Some are equally probable. Which to choose?

**Sampling** from a joint probability distribution involves generating a random sample that reflects the combined probabilites of multiple events occurring together.

There are many sampling methods.

- Inverse Transform Sampling

    1. Compute the cumulative distribution function (CDF)
    2. Generate a random number between 0 and 1
    3. Look up the corresponding possibility to that random number