# Transformer Model

## Encoder/Decoder RNN (Recurrent Neural Network)

Encoder takes words from sentences and encodes them into an underlying representation, an encoded context (could be a vector, many vectors). The order matters and is encoded in timestamps. The decoder reverses the process of encoding, converting it back to a human-readable sentence, perhaps in another language.

The encoder and decoder feed previous input into each subsequent step and uses that to predict the next word. The encoder and decoder each represent one recurrent neural network.

In a typical Encoder-Decoder model, especially in sequence-to-sequence (seq2seq) tasks such as machine translation:

The encoder processes the input sequence step-by-step. For each word or token in the input sequence, the encoder generates an intermediate representation.

The decoder then takes the final representation from the encoder and generates the translated sequence step-by-step.

Given the input sequence [How, are you] and the output sequence [你,好,嗎]:

The encoder would process each word in the input sequence one by one. So it would take 3 steps to encode the sequence [How, are, you].

The decoder would generate each word in the output sequence one by one. So it would take 3 steps to decode into the sequence [你,好,嗎].