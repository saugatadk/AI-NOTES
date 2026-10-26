# Appendix B: Essential Reading & Seminal Papers

A curated bibliography of foundational research papers and reading materials that underpin large language models and transformer architectures.

---

## 📄 Seminal Papers by Topic

### 1. Transformer Architecture & Attention
- **Attention Is All You Need** (Vaswani et al., 2017): Introduced the multi-head self-attention mechanism and the foundational transformer architecture.
- **FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness** (Dao et al., 2022): Hardware-aware optimization reducing memory reads/writes.
- **RoFormer: Enhanced Transformer with Rotary Position Embedding** (Su et al., 2021): Introduces RoPE relative position encoding used in LLaMA and modern LLMs.

### 2. GPT Foundations & Scaling
- **Improving Language Understanding by Generative Pre-Training** (GPT-1, Radford et al., 2018): First demonstration of generative pretraining followed by discriminative finetuning.
- **Language Models are Unsupervised Multitask Learners** (GPT-2, Radford et al., 2019): Demonstrates zero-shot task transfer at scale.
- **Language Models are Few-Shot Learners** (GPT-3, Brown et al., 2020): In-context learning and scaling dynamics.
- **Training Compute-Optimal Large Language Models** (Chinchilla, Hoffmann et al., 2022): Proves that tokens and parameters must scale in equal proportions.

### 3. Fine-Tuning, Parameter Efficiency & Alignment
- **LoRA: Low-Rank Adaptation of Large Language Models** (Hu et al., 2021): Freezes pretrained weights and injects trainable rank decomposition matrices.
- **QLoRA: Efficient Finetuning of Quantized LLMs** (Dettmers et al., 2023): Enables 4-bit NormalFloat fine-tuning with paged optimizers.
- **Training language models to follow instructions with human feedback** (InstructGPT, Ouyang et al., 2022): Introduces RLHF with PPO.
- **Direct Preference Optimization: Your Language Model is Secretly a Reward Model** (Rafailov et al., 2023): Mathematical simplification bypassing explicit reward models.