# AI Notes & Engineering Reference

A structured collection of notes, code implementations, and reference guides covering machine learning foundations, deep learning, large language models, generative AI agents, and production systems.

---

## Contents

### [0. Introductory Machine Learning](machine-learning-specialization-andrew-ng/README.md)
Lecture notes and lab assignments based on Andrew Ng's Machine Learning Specialization.
- Supervised learning (linear regression, logistic regression)
- Neural networks and multiclass classification
- Unsupervised algorithms (k-means clustering, anomaly detection)
- Recommender systems and reinforcement learning basics

### [1. Mathematics for Machine Learning](01-math-foundations/README.md)
Essential mathematical principles behind modern learning algorithms.
- Linear algebra, vector spaces, and matrix decompositions (SVD, Cholesky)
- Vector calculus, Jacobians, and gradient computation
- Probability distributions, continuous optimization, and Lagrange multipliers
- Hands-on tutorials for linear regression, PCA, and GMM implementations

### [2. Classical Machine Learning](02-classical-ml/README.md)
Concise reference sheets, mathematical formulas, and diagnostics for classical algorithms.
- Supervised algorithms (SVMs, decision trees, random forests, boosting)
- Unsupervised methods (clustering, PCA, dimensionality reduction)
- Diagnostic guides for bias-variance tradeoff, regularization, and model validation

### [3. Deep Learning Core & Computer Vision](03-deep-learning-core/README.md)
Comprehensive theory and PyTorch implementations adapted from *Dive into Deep Learning*.
- Multilayer perceptrons, backpropagation, and optimization techniques (SGD, Adam)
- Convolutional architectures (LeNet, AlexNet, ResNet, DenseNet) and object detection
- Recurrent neural networks (LSTM, GRU) and sequence modeling
- Self-attention mechanisms and transformer building blocks

### [4. Research Paper Implementations](04-sota-paper-implementations/README.md)
Readable PyTorch implementations of milestone deep learning research papers.
- Attention mechanisms, RoPE, and FlashAttention
- Generative modeling: DDPM, Stable Diffusion, and GANs
- Parameter-efficient fine-tuning (LoRA) and reinforcement learning (PPO, DQN)

### [5. Large Language Models From Scratch](05-llms-from-scratch/README.md)
Step-by-step implementation of an autoregressive GPT model in pure PyTorch, following Sebastian Raschka's guide.
- BPE tokenization and data pipeline setup
- Multi-head causal attention and full GPT-2 assembly
- Pretraining workflows, loss formulation, and weight loading
- Instruction fine-tuning, classification heads, and preference alignment

### [6. Applied Generative AI & Agents](06-applied-genai-and-agents/README.md)
Practical guides and tutorials for fine-tuning modern models and building agentic workflows.
- [Track 1: Fine-Tuning & Alignment](06-applied-genai-and-agents/01-finetuning-and-alignment/README.md) (SFT with TRL, LoRA/QLoRA, DPO/ORPO, vision-language models)
- [Track 2: Autonomous Agents](06-applied-genai-and-agents/02-agents-and-frameworks/README.md) (ReAct pattern, LangGraph, LlamaIndex, smolagents)
- [Track 3: Lab Notebooks](06-applied-genai-and-agents/notebooks/README.md) (interactive fine-tuning and agent labs)

### [7. MLOps & Production Systems](07-mlops-and-systems/README.md)
Bridging research code and maintainable production systems, based on Made With ML.
- Clean project structure, unit testing (`pytest`), and code quality
- Distributed training and hyperparameter tuning with Ray
- API serving with FastAPI and containerization
- CI/CD automation, model registries, and drift monitoring

---

## Acknowledgments

This repository brings together notes, exercises, and code implementations adapted from several open-source resources and courses:

- **Introductory ML**: [DeepLearning.AI / Coursera Machine Learning Specialization](https://www.coursera.org/specializations/machine-learning-introduction) and starter labs by [Peter Mulard](https://github.com/pmulard/machine-learning-specialization-andrew-ng)
- **Math Foundations**: [*Mathematics for Machine Learning*](https://github.com/mml-book/mml-book.github.io) by Marc Peter Deisenroth, A. Aldo Faisal, and Cheng Soon Ong
- **Classical ML**: [Stanford CS 229 Cheat Sheets](https://github.com/afshinea/stanford-cs-229-machine-learning) by Afshine Amidi and Shervine Amidi
- **Deep Learning**: [*Dive into Deep Learning (D2L)*](https://github.com/d2l-ai/d2l-en) by Aston Zhang, Zack C. Lipton, Mu Li, and Alexander J. Smola
- **Paper Implementations**: [*Annotated Deep Learning Paper Implementations*](https://github.com/labmlai/annotated_deep_learning_paper_implementations) by Varuna Jayasiri & labml.ai
- **LLMs From Scratch**: [*Build a Large Language Model (From Scratch)*](https://github.com/rasbt/LLMs-from-scratch) by Sebastian Raschka
- **Applied GenAI & Agents**: [*smol-course*](https://github.com/huggingface/smol-course) and [*agents-course*](https://github.com/huggingface/agents-course) by Hugging Face
- **MLOps**: [*Made With ML*](https://github.com/GokuMohandas/Made-With-ML) by Goku Mohandas
