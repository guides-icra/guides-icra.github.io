# **GUIDES**: **G**uidance **U**sing **I**nstructor-**D**istilled **E**mbeddings for Pre-trained Robot Policy Enhancement

[![Paper](https://img.shields.io/badge/Paper-arXiv-red)](https://arxiv.org/pdf/2511.03400.pdf)
[![Website](https://img.shields.io/badge/Website-GUIDES-blue)](https://guides-icra.github.io/)
[![ICRA](https://img.shields.io/badge/ICRA-2026-purple)](https://2026.ieee-icra.org/)
[![arXiv](https://img.shields.io/badge/arXiv-2511.03400-b31b1b.svg)](https://arxiv.org/abs/2511.03400)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

<p align="center">
  <img src="static/images/teaser.png" style="max-width: 75%; height: auto;">
  <br>
</p>

**GUIDES** is a lightweight framework that augments pre-trained robot policies with semantic guidance from foundation models without requiring architectural redesign.

[Minquan Gao](https://github.com/guides-icra)<sup>1</sup>,
[Xinyi Li](https://github.com/guides-icra)<sup>1</sup>,
[Qing Yan](https://github.com/guides-icra)<sup>1</sup>,
[Xiaojian Sun](https://github.com/guides-icra)<sup>1</sup>,
[Xiaopan Zhang](https://github.com/guides-icra)<sup>1</sup>,
[Chien-Ming Huang](https://www.cs.jhu.edu/~cmhuang/)<sup>2</sup>,
[Jiachen Li](https://jiachenli94.github.io/)<sup>1</sup>

<sup>1</sup> University of California, Riverside  
<sup>2</sup> Johns Hopkins University

## Overview

Pre-trained robot policies serve as the foundation of many validated robotic systems, which encapsulate extensive embodied knowledge. However, they often lack the semantic awareness characteristic of foundation models, and replacing them entirely is impractical in many situations due to high costs and the loss of accumulated knowledge. 

GUIDES addresses this gap by providing a lightweight framework that augments pre-trained policies with semantic guidance from foundation models without requiring architectural redesign.

## Key Features

- **Lightweight Integration:** Augments existing pre-trained policies without architectural redesign
- **Semantic Awareness:** Incorporates foundation model capabilities into robot policies
- **Instructor Module:** Fine-tuned vision-language model for contextual instruction generation
- **Guidance Embeddings:** Auxiliary module for encoding instructions into policy-compatible embeddings
- **Reflector Module:** LLM-based confidence monitoring and reasoning loop initiation
- **Inference-time Robustness:** Dynamic adaptation based on confidence levels

## Method

GUIDES employs a fine-tuned vision-language model (Instructor) to generate contextual instructions, which are encoded by an auxiliary module into guidance embeddings. These embeddings are injected into the policy's latent space, allowing the legacy model to adapt to this new semantic input through brief, targeted fine-tuning.

For inference-time robustness, a large language model-based Reflector monitors the Instructor's confidence and, when confidence is low, initiates a reasoning loop that analyzes execution history, retrieves relevant examples, and augments the VLM's context to refine subsequent actions.

## Results

- Extensive validation in the RoboCasa simulation environment across diverse policy architectures
- Consistent and substantial improvements in task success rates
- Real-world deployment on a UR5 robot demonstrating enhanced motion precision
- Practical and resource-efficient pathway to upgrade validated robot policies

## Website

Visit our [project website](https://guides-icra.github.io/) for more details, videos, and interactive content.

## Citation

If you find this work useful, please consider citing our paper:

```bibtex
@article{gao2025guides,
  title={GUIDES: Guidance Using Instructor-Distilled Embeddings for Pre-trained Robot Policy Enhancement},
  author={Gao, Minquan and Li, Xinyi and Yan, Qing and Sun, Xiaojian and Zhang, Xiaopan and Huang, Chien-Ming and Li, Jiachen},
  journal={IEEE International Conference on Robotics and Automation (ICRA)},
  year={2026}
}
```

## License

This project is licensed under the MIT License.