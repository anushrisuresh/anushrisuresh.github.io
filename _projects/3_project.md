---
layout: page
title: Semi-Supervised Reinforcement Learning for Autonomous Agents
description: Multi-modal RL framework with curiosity-driven exploration for adaptive policy learning in dynamic environments
img: assets/img/projects/RL/RL_thubmnail.png
importance: 3
category: work
related_publications: false
---

## Overview

This project develops a comprehensive framework that leverages self-supervised latent representations and curiosity-driven exploration for adaptive policy learning in dynamic environments. The work addresses the challenge of autonomous navigation in complex scenarios by combining multi-modal sensor fusion with advanced reinforcement learning techniques.

## Key Contributions

- **Multi-Modal Architecture**: Designed an encoder with semantic, depth, and LiDAR inputs processed through temporal GRUs
- **Self-Supervised Learning**: Implemented representation learning that reduces test loss to 0.0118
- **Curiosity-Driven Exploration**: Integrated Intrinsic Curiosity Module (ICM) with Proximal Policy Optimization (PPO)
- **Dynamic Adaptation**: Achieved 61.6% driving score on unseen maps after 1000 RL training episodes

## Technical Implementation

### Architecture Components

1. **ObservationTemporalEncoder**: Processes multi-modal sensor inputs across temporal sequences
2. **Proximal Policy Optimization (PPO)**: Ensures stable policy updates with clipped objectives
3. **Intrinsic Curiosity Module (ICM)**: Generates intrinsic rewards based on prediction errors
4. **Multi-Modal Fusion**: Combines semantic segmentation, depth, LiDAR, and metadata

### Training Pipeline

- **Pre-training**: Behavioral Cloning with PPO-ICM initialization
- **Active Learning**: Fine-tuning in altered CARLA environments
- **Evaluation**: CARLA Leaderboard driving score metrics

## Results

The framework demonstrates significant improvements in adaptability under dynamic conditions:

- **Representation Learning**: Test loss reduced to 0.0118
- **Driving Performance**: 61.6% driving score on unseen test maps
- **Generalization**: Robust performance across weather variations and dynamic obstacles

## Applications

This research has direct applications in:

- Autonomous vehicle navigation
- Robotic exploration in unknown environments
- Multi-modal sensor fusion for decision-making
- Adaptive AI systems in dynamic scenarios

**GitHub Repository**: [ML-DL-Fall2024/semi-supervised-learning](https://github.com/ML-DL-Fall2024/semi-supervised-learning)

**Technologies**: PyTorch, CARLA Simulator, Reinforcement Learning, Computer Vision, Deep Learning, ROS
