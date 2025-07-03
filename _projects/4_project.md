---
layout: page
title: Super-Resolution Enhanced Face Recognition
description: Improving face recognition accuracy on low-quality surveillance images using GANs
img: assets/img/projects/face_rec/face_rec_thumbnail.webp
importance: 4
category: work
giscus_comments: true
---

## Super-Resolution Enhanced Face Recognition

This project addresses the critical challenge of face recognition in surveillance systems where captured images are often of poor quality due to distance, lighting conditions, or camera limitations. By implementing a Super-Resolution Generative Adversarial Network (SR-GAN), we significantly improve recognition accuracy on low-quality face images.

### Problem Statement

Surveillance cameras frequently capture face images that are:
- **Low Resolution**: Limited pixel information due to distance or camera constraints
- **Poor Quality**: Affected by lighting, motion blur, or compression artifacts  
- **Challenging for Recognition**: Standard face recognition systems struggle with degraded inputs

### Technical Approach

#### Super-Resolution GAN Architecture
- **Generator Network**: Transforms low-resolution inputs to high-resolution outputs
- **Discriminator Network**: Ensures realistic and high-quality super-resolved images
- **Adversarial Training**: Generator and discriminator compete to improve image quality
- **Perceptual Loss**: Maintains facial features and identity-relevant information

#### Integration with Face Recognition
- **Two-Stage Pipeline**: Super-resolution followed by face recognition
- **End-to-End Optimization**: Joint training for optimal recognition performance
- **Feature Preservation**: Maintains discriminative facial characteristics during upsampling

### Performance Achievements

#### Quantitative Results
- **37% Improvement**: Recognition rate increase on down-sampled test images
- **5% Overall Gain**: Performance improvement across the entire proprietary dataset
- **Robust Performance**: Consistent improvements across various quality degradations

#### Technical Metrics
- **PSNR Enhancement**: Significant peak signal-to-noise ratio improvements
- **SSIM Scores**: Better structural similarity to high-quality references
- **Recognition Accuracy**: Substantial gains in face identification tasks

### Dataset & Evaluation

- **Proprietary Surveillance Dataset**: Real-world low-quality face images
- **Diverse Conditions**: Various lighting, angles, and quality degradations
- **Comprehensive Testing**: Multiple resolution levels and quality metrics
- **Baseline Comparisons**: Performance against standard recognition systems

### Applications & Impact

This technology has significant implications for:

- **Security Systems**: Enhanced surveillance and access control
- **Law Enforcement**: Improved suspect identification from CCTV footage
- **Border Control**: Better passport and ID verification systems
- **Commercial Applications**: Retail analytics and customer recognition

### Technical Innovation

- **Domain-Specific Training**: Tailored for surveillance image characteristics
- **Quality-Aware Processing**: Adaptive enhancement based on input degradation
- **Real-Time Capability**: Optimized for practical deployment scenarios
- **Scalable Architecture**: Efficient processing for large-scale surveillance networks

The project demonstrates how generative adversarial networks can be effectively applied to enhance face recognition systems, particularly in challenging real-world surveillance scenarios where image quality is often compromised.

**GitHub Repository**: [anushrisuresh/LRFR](https://github.com/anushrisuresh/LRFR)

**Technologies**: GANs, Super-Resolution, Face Recognition, Computer Vision, Deep Learning, PyTorch
