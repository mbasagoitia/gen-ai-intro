# The Chain Rule of Probabilities

For large numbers of possibilities, how can we simplify the calculation of join probabilities?

The **chain rule of probabilities** states that the joint probability of a sequence of events occurring is the product of the probabilities of each event given that the preceding events have occurred.

p(x1, x2, x3) = p(x1) * p(x2 | x1) * p(x3 | x1, x2)

Essentially, multiply all of the conditional probabilities that led up to a specific event.