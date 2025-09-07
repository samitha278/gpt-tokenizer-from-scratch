# gpt-tokenizer-from-scratch
An implementation of the GPT Tokenizer built from scratch.





## References

- [Byte Pair Encoding (BPE) algorithm](https://en.wikipedia.org/wiki/Byte-pair_encoding)  
- [Language Models are Unsupervised Multitask Learners – §2.2 Input Representation](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)  
- [OpenAI GPT-2 Encoder Implementation](http://github.com/openai/gpt-2/blob/master/src/encoder.py)  
- [OpenAI tiktoken (public extension)](https://github.com/openai/tiktoken/blob/main/tiktoken_ext/openai_public.py)


#### Input Representation

GPT’s tokenizer tweaks BPE to avoid wasting slots on variants like `dog`, `dog.`, `dog!`.  
It blocks merges between letters and punctuation (except spaces), making vocab more efficient while still handling any Unicode text.


