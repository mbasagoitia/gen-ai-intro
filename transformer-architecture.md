# Transformer's Architecture

## Embedding

The model has access to a vocabulary of words in a certain language, like English, where each word/token has an id and embedding vector with several dimensions. We feed the vector representation of each word/token to the transformer.

## Positional Encoding

We need to add position information to the embedding vector, which is a position vector of the same size (# of dimensions) added to each embedding vector. Calculated by sampling sine/cosine waves with increasingly higher frequencies. Position vectors must be unique.

## Outputs of the Transformer Model

The output is a probability rather than a whole word. At each timestamp, a matrix of tokens and vocabulary words with the probability that a word is output for each token is generated. At each step, the output (determined by the probability) is fed into the decoder and the next matrix is generated. The transformer decoder is non-deterministic because it has some random processes (probabilities) that may randomly be chosen differently each time.