# The AI Master Knowledge Base

A comprehensive, centralized study workspace and code reference covering the foundational **Artificial Intelligence** — spanning pure mathematical principles, classical algorithms, deep learning architectures, paper implementations, foundation LLMs, applied GenAI agents, and production MLOps systems.

---

## 🧭 Master Curriculum & Recommended Study Order

| Step | Pillar | Coverage | Local Directory | Key Topics Mastered |
| :---: | :--- | :---: | :--- | :--- |
| **0** | **Introductory ML** | *Foundational* | [machine-learning-specialization-andrew-ng](machine-learning-specialization-andrew-ng/) | Supervised learning, neural nets, k-means, PCA, recommender systems |
| **1** | **Math Foundations** | **~10%** | [01-math-foundations](01-math-foundations/) | Linear algebra, matrix calculus, SVD/PCA, probability distributions |
| **2** | **Classical ML & Guides** | **~15%** | [02-classical-ml](02-classical-ml/) | SVMs, decision trees, ensemble methods, clustering, high-yield formula sheets |
| **3** | **Deep Learning & CV** | **~25%** | [03-deep-learning-core](03-deep-learning-core/) | Backprop, CNNs, ResNet, object detection, RNNs, attention mechanisms |
| **4** | **SOTA Architectures** | **~10%** | [04-sota-paper-implementations](04-sota-paper-implementations/) | ViT, Diffusion (DDPM), GANs, RoPE, LoRA, RL (PPO/DQN) in pure PyTorch |
| **5** | **LLM Internals** | **~10%** | [05-llms-from-scratch](05-llms-from-scratch/) | BPE tokenizers, multi-head causal attention, GPT-2 from scratch, SFT |
| **6** | **GenAI & Agents** | **~10%** | [06-applied-genai-and-agents](06-applied-genai-and-agents/) | Quantization (GGUF/AWQ), PEFT (QLoRA), alignment (DPO/ORPO), RAG, Agents |
| **7** | **MLOps & Systems** | **~10%** | [07-mlops-and-systems](07-mlops-and-systems/) | Distributed training, Ray, FastAPI serving, CI/CD, data drift monitoring |

---

## 🗂️ Pillar Breakdown

### 0. Introductory ML Foundations
- **Path**: [machine-learning-specialization-andrew-ng/](machine-learning-specialization-andrew-ng/)
- **Core Topics**: Andrew Ng's 3-course specialization covering regression, neural networks, decision trees, anomaly detection, recommender systems, and reinforcement learning.
- **Resources**: Interactive Jupyter notebooks in `assignments/` and topic summaries in `notes/`.

### 1. Mathematical Foundations (~10% of AI)
- **Path**: [01-math-foundations/](01-math-foundations/)
- **Core Topics**: Strips out pure-math abstractions to focus on the equations that power machine learning.
- **Key Modules**:
  - Linear Algebra & Vector Spaces
  - Matrix Decompositions (SVD, Cholesky, Eigendecomposition)
  - Vector Calculus, Gradients & Jacobians
  - Probability Distributions & Continuous Optimization
- **Tutorial Notebooks**: [Linear Regression](01-math-foundations/tutorials/tutorial_linear_regression.ipynb), [PCA](01-math-foundations/tutorials/tutorial_pca.ipynb), [GMM](01-math-foundations/tutorials/tutorial_gmm.ipynb).

### 2. Classical Machine Learning & Formula Guides (~15% of AI)
- **Path**: [02-classical-ml/](02-classical-ml/)
- **Core Topics**: High-yield visual reference sheets and mathematical formulas for rapid review.
- **Cheat Sheets**:
  - [Super Cheatsheet for Machine Learning](02-classical-ml/super-cheatsheet-machine-learning.pdf)
  - [Supervised Learning Guide](02-classical-ml/cheatsheet-supervised-learning.pdf)
  - [Unsupervised Learning Guide](02-classical-ml/cheatsheet-unsupervised-learning.pdf)
  - [Deep Learning Summary](02-classical-ml/cheatsheet-deep-learning.pdf)
  - [Tips, Tricks & Diagnostics](02-classical-ml/cheatsheet-machine-learning-tips-and-tricks.pdf)

### 3. Deep Learning Core, CV & Modern Architectures (~25% of AI)
- **Path**: [03-deep-learning-core/](03-deep-learning-core/)
- **Core Topics**: Comprehensive interactive curriculum integrating mathematical theory and runnable PyTorch code side-by-side.
- **Key Chapters**:
  - [Multilayer Perceptrons & Backpropagation](03-deep-learning-core/chapter_multilayer-perceptrons)
  - [Convolutional Neural Networks & Modern CNNs](03-deep-learning-core/chapter_convolutional-neural-networks)
  - [Computer Vision & Object Detection](03-deep-learning-core/chapter_computer-vision)
  - [Modern Recurrent Networks (LSTM/GRU)](03-deep-learning-core/chapter_recurrent-modern)
  - [Attention Mechanisms & Transformers](03-deep-learning-core/chapter_attention-mechanisms-and-transformers)

### 4. SOTA Paper Implementations & Generative Vision (~10% of AI)
- **Path**: [04-sota-paper-implementations/](04-sota-paper-implementations/)
- **Core Topics**: Line-by-line PyTorch implementations of breakthrough AI research papers.
- **Key Modules**:
  - [Transformers, RoPE, ALiBi, & FlashAttention](04-sota-paper-implementations/labml_nn/transformers/)
  - [Diffusion Models (DDPM & Stable Diffusion)](04-sota-paper-implementations/labml_nn/diffusion/)
  - [Generative Adversarial Networks (WGAN/StyleGAN)](04-sota-paper-implementations/labml_nn/gan/)
  - [Parameter-Efficient Tuning (LoRA)](04-sota-paper-implementations/labml_nn/lora/)
  - [Reinforcement Learning (PPO & DQN)](04-sota-paper-implementations/labml_nn/rl/)

### 5. Large Language Models (LLMs) From Scratch (~10% of AI)
- **Path**: [05-llms-from-scratch/](05-llms-from-scratch/)
- **Core Topics**: Step-by-step implementation of an end-to-end GPT foundational model in pure PyTorch.
- **Key Chapters**:
  - [Ch 02: BPE Tokenization & Data Pipelines](05-llms-from-scratch/ch02/)
  - [Ch 03: Multi-Head Causal Attention](05-llms-from-scratch/ch03/)
  - [Ch 04: Full GPT-2 Architecture Assembly](05-llms-from-scratch/ch04/)
  - [Ch 05: Pretraining & Weight Loading](05-llms-from-scratch/ch05/)
  - [Ch 06-07: Fine-Tuning & Instruction Alignment](05-llms-from-scratch/ch06/)

### 6. Applied GenAI, RAG, Fine-Tuning & AI Agents (~10% of AI)
- **Path**: [06-applied-genai-and-agents/](06-applied-genai-and-agents/)
- **Core Topics**: Hands-on curriculum covering modern fine-tuning, parameter-efficiency, preference alignment, and production AI agent frameworks.
- **Key Modules**:
  - [Track 1: Fine-Tuning & Alignment](06-applied-genai-and-agents/01-finetuning-and-alignment/) (SFT, LoRA/PEFT, DPO/ORPO, VLMs)
  - [Track 2: AI Agents & Frameworks](06-applied-genai-and-agents/02-agents-and-frameworks/) (ReAct loop, Tools, LangGraph, LlamaIndex, smolagents)
  - [Track 3: Hands-On Notebooks](06-applied-genai-and-agents/notebooks/)

### 7. ML System Design, MLOps & Production (~10% of AI)
- **Path**: [07-mlops-and-systems/](07-mlops-and-systems/)
- **Core Topics**: Bridging the gap between Jupyter prototypes and scalable, production-grade AI systems.
- **Key Focus Areas**:
  - Clean architecture, testing (`pytest`), and packaging
  - Distributed training and hyperparameter tuning with Ray
  - High-throughput REST API serving with FastAPI
  - CI/CD automation and model registry
  - Data drift monitoring and automated retraining pipelines

---

## 📑 Acknowledgments & Sources

This knowledge base is curated and maintained as a structured personal learning workspace. Subtle attribution and credit go to the following authors and open-source projects whose high-quality foundational materials were adapted to build these pillars:

1. **Mathematical Foundations**: Adapted from *Mathematics for Machine Learning* by [Marc Peter Deisenroth, A. Aldo Faisal, and Cheng Soon Ong](https://github.com/mml-book/mml-book.github.io).
2. **Classical Machine Learning**: Adapted from Stanford CS 229 VIP cheat sheets by [Afshine Amidi & Shervine Amidi](https://github.com/afshinea/stanford-cs-229-machine-learning).
3. **Deep Learning Core**: Adapted from *Dive into Deep Learning (D2L)* by [Aston Zhang, Zack C. Lipton, Mu Li, Alexander J. Smola](https://github.com/d2l-ai/d2l-en).
4. **SOTA Implementations**: Adapted from *Annotated Deep Learning Paper Implementations* by [Varuna Jayasiri & labml.ai](https://github.com/labmlai/annotated_deep_learning_paper_implementations).
5. **LLMs From Scratch**: Adapted from *Build a Large Language Model (From Scratch)* by [Sebastian Raschka](https://github.com/rasbt/LLMs-from-scratch).
6. **Applied GenAI & Agents**: Adapted from Hugging Face's [*smol-course*](https://github.com/huggingface/smol-course) and [*agents-course*](https://github.com/huggingface/agents-course), with reference architecture concepts from [Maxime Labonne](https://github.com/mlabonne/llm-course).
7. **MLOps & System Design**: Adapted from *Made With ML* by [Goku Mohandas](https://github.com/GokuMohandas/Made-With-ML).
8. **Introductory ML Specialization**: Adapted from Coursera's Machine Learning Specialization by [Andrew Ng (DeepLearning.AI)](https://www.coursera.org/specializations/machine-learning-introduction) and starter labs by [Peter Mulard](https://github.com/pmulard/machine-learning-specialization-andrew-ng).
