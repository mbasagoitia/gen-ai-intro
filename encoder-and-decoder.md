# Encoder

The encoder has two layers; we generally train two different networks: one that handles **rules** to extract new meanings, and the other that handles **context**.

2 blocks:

- Attention: creates relevent context groups
- FFN (feed forward network): applies new rules to get new features

# Decoder

Includes FFN and self-attention, with the addition of cross-attention layer (linked from encoder)