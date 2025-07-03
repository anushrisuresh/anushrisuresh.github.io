---
layout: page
title: Selective KV Quantization
description: Don't Drop It, Compress It - Reducing LLM KV cache memory usage by ~2x with minimal accuracy loss
img: assets/img/kv_quantization_preview.jpg
importance: 1
category: work
giscus_comments: true
---

## Don't Drop It, Compress It: Selective KV Quantization

Modern large language models (LLMs) rely on a **Key–Value (KV) cache** to store intermediate representations for long‐context generation, but this cache can consume **90%+ of GPU memory** as sequence length grows. Existing solutions either **drop** old tokens (sliding window, attention sinks) or **uniformly compress** all tokens, often trading off accuracy for memory.

**Selective KV Quantization** bridges this gap by:

1. **Preserving** "sink" (initial prompt) and a sliding "window" of recent tokens in full precision (FP16)
2. **Aggressively quantizing** older tokens to int8
3. **Dequantizing on‐the‐fly** only when needed for attention

This hybrid strategy delivers up to **2× memory savings** with **no increase in perplexity** (5.56) and only a **minor drop in ROUGE-L** (0.2073 → 0.1709).

### Key Results

| Caching Strategy | Perplexity | ROUGE-L | Memory Reduction |
|------------------|------------|---------|------------------|
| Full Cache       | 5.56       | 0.2073  | Baseline         |
| Compressed Cache | 132.08     | 0.1030  | ~4×              |
| **Quantized Cache** | **5.56**   | **0.1709** | **~2×**          |

### Technical Highlights

- **Memory Efficiency**: KV cache accounts for over 90% of total GPU memory usage
- **Accuracy Preservation**: Maintains full-cache perplexity while achieving significant memory savings  
- **Selective Strategy**: Smart preservation of important tokens (sink + sliding window) in full precision
- **On-the-fly Processing**: Efficient dequantization only when needed for attention computation

### Implementation

The project includes comprehensive evaluation scripts, PyTorch profiler integration, and support for various compression strategies. The codebase is built on top of PyTorch and optimized for CUDA-enabled GPUs.

**GitHub Repository**: [anushrisuresh/kv-quantization](https://github.com/anushrisuresh/kv-quantization)

**Technologies**: PyTorch, CUDA, Python, Quantization, Large Language Models
