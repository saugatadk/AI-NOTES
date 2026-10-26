# Building Large Language Models From Scratch

A hands-on implementation guide and code repository for developing, pretraining, and finetuning a GPT-style foundational large language model in pure PyTorch.

---

## 🧭 Step-by-Step Architecture Roadmap

### [Chapter 1: Understanding Large Language Models](ch01/)
- Foundations of transformer-based LLMs
- Autoregressive next-token prediction
- High-level architecture and stage overview

### [Chapter 2: Working with Text Data](ch02/)
- Byte-Pair Encoding (BPE) tokenization
- Vocabulary building and token embedding lookup
- Positional embeddings and context window formulation
- PyTorch Dataset and DataLoader pipelines

### [Chapter 3: Coding Attention Mechanisms](ch03/)
- Scaled Dot-Product Attention from scratch
- Causal attention masking (autoregressive decoding)
- Multi-Head Attention implementation and tensor reshaping

### [Chapter 4: Implementing a GPT Model from Scratch](ch04/)
- Transformer block assembly
- Layer Normalization and GELU activation
- Feedforward networks and residual connections
- Full GPT-2 architecture assembly (124M parameters)

### [Chapter 5: Pretraining on Unlabeled Text Data](ch05/)
- Cross-entropy loss formulation and perplexity
- Training loop implementation with AdamW optimizer
- Autoregressive text generation with top-k sampling and temperature
- Loading pretrained OpenAI GPT-2 weights

### [Chapter 6: Finetuning for Text Classification](ch06/)
- Replacing the output head for classification tasks
- Transfer learning on domain-specific datasets (Spam classification)
- Evaluation metrics and training dynamics

### [Chapter 7: Instruction Finetuning & Alignment](ch07/)
- Instruction dataset preparation and prompt formatting
- Supervised instruction tuning (SFT)
- Alignment foundations (RLHF / DPO concepts)

---

## 📑 Appendices
- [Appendix A: Introduction to PyTorch](appendix-A/)
- [Appendix B: Neural Network Training Essentials](appendix-B/)
- [Appendix C: Exercises and Solutions](appendix-C/)
- [Appendix D: Adding Bells and Whistles to Training](appendix-D/)
- [Appendix E: Parameter-Efficient Fine-Tuning (LoRA)](appendix-E/)
