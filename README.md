# gpt-tokenizer-from-scratch
An implementation of the GPT Tokenizer built from scratch.





## References

- [Byte Pair Encoding (BPE) algorithm](https://en.wikipedia.org/wiki/Byte-pair_encoding)  
- [Language Models are Unsupervised Multitask Learners – §2.2 Input Representation](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)

### Input Representation

Standard BPE often wastes vocabulary slots by creating separate tokens for common word variants like `dog`, `dog.`, `dog!`, `dog?`.  
To fix this, GPT’s tokenizer prevents merges across character categories (letters vs punctuation), with one exception: spaces.  
This keeps words compact, improves compression, and still allows the model to tokenize **any Unicode string** without unknown tokens.

