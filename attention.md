# Attention

A drawback of RNN is that the longer it gets, the harder it is to retain or "remember" context.

A decoder can pose a query, such as sentence subject, verb, etc. and reference the most relevant link (such as a "subject" key) to the encoder to gain additional context. This is known as an "attention" step. This mechanism helps us achieve long-term depedency.

The attention mechanism, specifically the query-key-value (QKV) paradigm, is used in models like Transformers to capture dependencies between words or tokens in a sequence. Let's break down the relation of this cognitive process to the QKV:

Query: This represents the item you're currently focused on or considering. In the example given, when reading "eat", the question or the context formed in the mind is "what is eaten?".

Key: The keys represent all the possible items you could be considering in relation to the query. In this case, the contextual understanding of something being "edible" relates to the action of "eat".

Value: The values are the actual items or details you retrieve based on how well the keys matched the query. If "edible" matches well with "what is eaten?", then you retrieve or focus on the actual word or concept, which is "eat" in this case.

Encoder only uses self attention, and decoder uses both cross and self-attention.

**Cross attention:** As we are decoding the sentence, we get information from the input sentence (encoder).

**Self attention:** Additional layer where context is derived from itself.

Encoding: The Transformer's encoder processes the entire input sequence [How, are, you] simultaneously in a single step. This is made possible by the self-attention mechanism which allows each word/token in the sequence to attend to all other words in the sequence, all at once. Thus, the encoding happens in 1 step.

Decoding: For the decoding part, while the Transformer's decoder also employs the self-attention mechanism, it typically generates the output sequence one token at a time, especially in a translation task. For the output sequence [你,好,嗎], the decoder would generate each token in 3 steps.

Cross-attention to “who”, “are”, “you” - As the decoder generates the token "tu", it uses cross-attention to attend to the input tokens "who", "are", and "you" to gather context.

Self-attention to “qui”, “es” - As the decoder generates the token "tu", it also uses self-attention to attend to previously generated tokens in the output sequence ("qui" and "es") for context.