---
layout: page
title: Rich Teacher Features for Efficient Single-Image Haze Removal
description: Lightweight image dehazing using feature distillation and affinity modules
img: assets/img/projects/Dehaze/Knowledge-Distillation_thumbnail.webp
importance: 2
category: work
giscus_comments: true
---

## Rich Teacher Features for Efficient Single-Image Haze Removal

Single-image haze removal is a challenging computer vision task that significantly impacts image quality and downstream applications. This project introduces a novel lightweight framework that leverages **heterogeneous knowledge distillation** from super-resolution models to achieve efficient and effective image dehazing.

### Key Innovation: Feature Affinity Module

Our approach exploits rich "dark-knowledge" information from a lightweight pre-trained super-resolution teacher model through a specially designed **Feature Affinity Module** that maximizes the flow of semantic features to the student dehazing network.

### Technical Approach

1. **Heterogeneous Knowledge Distillation**: Transfer knowledge from super-resolution domain to dehazing
2. **Feature Affinity Module**: Designed to maximize rich feature semantic flow
3. **Lightweight Architecture**: Significantly reduced model complexity while maintaining performance
4. **Plug-and-Play Design**: Can be integrated with existing baseline models

### Results & Performance

- **PSNR Improvement**: Up to 15% gains in Peak Signal-to-Noise Ratio
- **Model Efficiency**: ~20× reduction in model size compared to traditional approaches
- **Dataset Validation**: Comprehensive evaluation on RESIDE-Standard dataset
- **Robustness**: Demonstrated effectiveness on both synthetic and real-world domains

### Architecture Highlights

The framework employs a dual-path architecture with:

- **Clear Feature Maps (F.M)**: Processing clean image features
- **Hazy Feature Maps (F.M)**: Processing degraded input features
- **Pooling and Flattening**: Efficient feature dimensionality reduction
- **L2 Loss Optimization**: Robust training objective for feature alignment

### Applications

This lightweight dehazing solution is particularly suitable for:

- **Edge Computing**: On-device image enhancement
- **Real-time Processing**: Low-latency applications
- **Resource-Constrained Environments**: Mobile and embedded systems
- **Surveillance Systems**: Improving visibility in adverse weather conditions

**GitHub Repository**: [anushrisuresh/Dehaze](https://github.com/anushrisuresh/Dehaze)

**Technologies**: PyTorch, Computer Vision, Knowledge Distillation, Image Processing, Deep Learning
