# Flow-Matching-From-Scratch-Training-Distillation

An end-to-end Flow Matching implementation built from scratch, based on the **'scale-at-all-cost'** parameter from [arXiv:2511.22699](https://arxiv.org/abs/2511.22699) (Z-image). This repository unifies the entire pipeline from data curation and architecture design to distillation and inference acceleration.

---

## Goals

This project will demonstrate the theoretical and practical foundations of Flow Matching at scale. The primary objectives are:

- **Data Curation:** We will implement robust data pipelines including filtering, quality assessment, and preprocessing strategies aligned with scale-at-all-cost principles.

- **Model Architecture:** We will design and train a Flow Matching model from scratch, exploring architectural choices  optimized for efficient scaling.

- **Training:** We will train the model on a **single H100 GPU**, validating the theoretical claims around scaling behavior and training dynamics.

- **Distillation:** We will apply state-of-the-art distribution matching distillation techniques to compress the trained model while preserving generation quality, targeting few-step inference. Specifically, we will explore:
  - [DMDR: Distribution Matching Distillation Meets Reinforcement Learning](https://arxiv.org/abs/2511.13649) — combining distribution matching with RL-based fine-tuning for improved sample quality.
  - [Decoupled DMD: CFG Augmentation as the Spear, Distribution Matching as the Shield](https://arxiv.org/abs/2511.22677) — decoupling classifier-free guidance from distribution matching for more stable distillation.

- **Inference Acceleration:** We will implement and benchmark inference optimizations with a primary focus on **caching strategies** , attention caching to minimize redundant computation during sampling.

---

## References

- [Flow Matching for Generative Modeling](https://arxiv.org/abs/2210.02747)
- [Z-image: Scale-at-All-Cost](https://arxiv.org/abs/2511.22699)
- [Scalable Diffusion Models with Transformers (DiT)](https://arxiv.org/abs/2212.09748)
- [DMDR: Distribution Matching Distillation Meets Reinforcement Learning](https://arxiv.org/abs/2511.13649)
- [Decoupled DMD: CFG Augmentation as the Spear, Distribution Matching as the Shield](https://arxiv.org/abs/2511.22677)

---

## License

MIT License
