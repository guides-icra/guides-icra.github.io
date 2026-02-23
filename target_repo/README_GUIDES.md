# GUIDES: Guidance Using Instructor-Distilled Embeddings for Pre-trained Robot Policy Enhancement

This is the project page for "GUIDES: Guidance Using Instructor-Distilled Embeddings for Pre-trained Robot Policy Enhancement" submitted to ICRA 2026.

## Abstract

Pre-trained robot policies serve as the foundation of many validated robotic systems, which encapsulate extensive embodied knowledge. However, they often lack the semantic awareness characteristic of foundation models, and replacing them entirely is impractical in many situations due to high costs and the loss of accumulated knowledge. To address this gap, we introduce GUIDES, a lightweight framework that augments pre-trained policies with semantic guidance from foundation models without requiring architectural redesign.

GUIDES employs a fine-tuned vision-language model (Instructor) to generate contextual instructions, which are encoded by an auxiliary module into guidance embeddings. These embeddings are injected into the policy's latent space, allowing the legacy model to adapt to this new semantic input through brief, targeted fine-tuning. For inference-time robustness, a large language model-based Reflector monitors the Instructor's confidence and, when confidence is low, initiates a reasoning loop that analyzes execution history, retrieves relevant examples, and augments the VLM's context to refine subsequent actions.

## Authors

- Marvin Qing Xinyi (University of California, Riverside) - *Co-first author*
- Chieng Ming Huang (Johns Hopkins University) - *Corresponding author*
- Jiachen Li (University of California, Riverside) - *Corresponding author*

## Links

- [Paper (arXiv)](https://arxiv.org/pdf/2511.03400.pdf)
- [arXiv](https://arxiv.org/abs/2511.03400)
- Code (Coming Soon)

## Citation

```bibtex
@article{xinyi2025guides,
  title={GUIDES: Guidance Using Instructor-Distilled Embeddings for Pre-trained Robot Policy Enhancement},
  author={Xinyi, Marvin Qing and Huang, Chieng Ming and Li, Jiachen},
  journal={arXiv preprint arXiv:2511.03400},
  year={2025},
  note={Submitted to ICRA 2026}
}
```

## Website

This website is built using the Academic Project Page Template. Visit [https://guides-icra.github.io/](https://guides-icra.github.io/) to view the full project page.

## Key Features

- **Lightweight Framework**: Augments pre-trained policies without architectural redesign
- **Instructor-Distilled Embeddings**: Uses fine-tuned VLM to generate contextual guidance
- **Reflector Component**: LLM-based monitoring for inference-time robustness
- **Practical Deployment**: Validated on both simulation (RoboCasa) and real-world (UR5) systems

## Framework Components

1. **Instructor**: A fine-tuned vision-language model that generates contextual instructions based on visual observations
2. **Guidance Embeddings**: An auxiliary module that encodes instructions into embeddings that are injected into the policy's latent space
3. **Reflector**: A large language model-based component that monitors confidence and initiates reasoning loops when needed

## Results

Extensive validation in the RoboCasa simulation environment across diverse policy architectures shows consistent and substantial improvements in task success rates. Real-world deployment on a UR5 robot further demonstrates that GUIDES enhances motion precision for critical sub-tasks such as grasping.

## License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.