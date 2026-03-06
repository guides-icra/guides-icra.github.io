# GUIDES: Guidance Using Instructor-Distilled Embeddings for Pre-trained Robot Policy Enhancement

This repository contains the project website for **GUIDES**, a lightweight framework that augments pre-trained robot policies with semantic guidance from foundation models.

## Abstract

Pre-trained robot policies serve as the foundation of many validated robotic systems, which encapsulate extensive embodied knowledge. However, they often lack the semantic awareness characteristic of foundation models, and replacing them entirely is impractical in many situations due to high costs and the loss of accumulated knowledge.

To address this gap, we introduce **GUIDES**, a lightweight framework that augments pre-trained policies with semantic guidance from foundation models without requiring architectural redesign. GUIDES employs a fine-tuned vision-language model (Instructor) to generate contextual instructions, which are encoded by an auxiliary module into guidance embeddings. These embeddings are injected into the policy's latent space, allowing the legacy model to adapt to this new semantic input through brief, targeted fine-tuning.

## Authors

- **Minquan Gao**¹'²* - Johns Hopkins University
- **Xinyi Li**²* - Johns Hopkins University  
- **Qing Yan**²* - Johns Hopkins University
- **Xiaojian Sun**² - Johns Hopkins University
- **Xiaopan Zhang**¹ - University of California, Riverside
- **Chien-Ming Huang**²‡ - Johns Hopkins University
- **Jiachen Li**¹‡ - University of California, Riverside

*Equal contribution  
‡Corresponding authors

## Organizations

- [Intuitive Computing Lab at Johns Hopkins University](https://intuitivecomputing.github.io/)
- Trustworthy Autonomous Systems Laboratory (TASL)

## Links

- **Paper**: [arXiv:2511.03400](https://arxiv.org/abs/2511.03400)
- **Code**: Coming Soon
- **Website**: [https://guides-icra.github.io](https://guides-icra.github.io)

## Citation

```bibtex
@article{gao2024guides,
  title={GUIDES: Guidance Using Instructor-Distilled Embeddings for Pre-trained Robot Policy Enhancement},
  author={Gao, Minquan and Li, Xinyi and Yan, Qing and Sun, Xiaojian and Zhang, Xiaopan and Huang, Chien-Ming and Li, Jiachen},
  journal={arXiv preprint arXiv:2511.03400},
  year={2024}
}
```

## Website Template

This website is built using the template from [Nerfies](https://github.com/nerfies/nerfies.github.io).