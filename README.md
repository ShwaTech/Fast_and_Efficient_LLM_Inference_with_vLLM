# 🚀 Fast & Efficient LLM Inference with vLLM

> Optimize, deploy, and benchmark Large Language Models using LLM Compressor, vLLM, GuideLLM, and lm-eval.

![Python](https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge\&logo=python)
![vLLM](https://img.shields.io/badge/vLLM-LLM%20Serving-green?style=for-the-badge)
![LLM](https://img.shields.io/badge/LLM-Inference-orange?style=for-the-badge)
![AI](https://img.shields.io/badge/Artificial-Intelligence-red?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-success?style=for-the-badge)

## 📖 Overview

Modern Large Language Models require enormous GPU memory during inference. Efficient deployment is essential to reduce latency, maximize throughput, and minimize infrastructure costs while maintaining high model quality.

This project demonstrates a complete **LLM optimization and deployment pipeline** using open-source tools. Starting from a full-precision **Qwen** model, the workflow compresses the model through quantization, serves it with **vLLM**, and benchmarks its performance under realistic workloads.

The project explores how modern inference engines efficiently manage GPU memory through:

**`Model Optimization`**:

* LLM Compressor
* Weight Quantization

**`Inference Optimization`**:

* Continuous Batching
* PagedAttention
* Prefix Caching
* KV Cache Optimization

---

## 🎯 Objectives

* Understand the architecture of LLM inference
* Reduce GPU memory consumption
* Increase inference throughput
* Reduce latency
* Deploy production-ready inference servers
* Benchmark serving performance
* Evaluate model quality after compression

---

## 🏗️ Project Workflow

```text
Full Precision Qwen Model
            │
            ▼
       Quantization
     (LLM Compressor)
            │
            ▼
     Compressed Model
            │
            ▼
     Deploy with vLLM
            │
            ▼
    OpenAI Compatible API
            │
            ▼
    Benchmark (GuideLLM)
            │
            ▼
 Evaluate Accuracy (lm-eval)
```

---

## ⚡ Technologies Used

| Technology     | Purpose                      |
| -------------- | ---------------------------- |
| Python         | Development                  |
| Qwen           | Open-source LLM              |
| LLM Compressor | Model Quantization           |
| vLLM           | High-performance LLM Serving |
| GuideLLM       | Load Testing                 |
| lm-eval        | Model Evaluation             |
| OpenAI API     | Client Interface             |

---

## 🧠 Concepts Covered

### LLM Inference

Understanding what happens when an LLM generates tokens.

Topics include:

* Tokenization
* Transformer Forward Pass
* GPU Memory Usage
* KV Cache
* Attention Mechanism

### Quantization

Reduced model size while preserving performance.

Benefits:

* Lower GPU memory usage
* Faster inference
* Reduced deployment cost
* Higher throughput

Evaluation metric:

* Perplexity

### KV Cache

The project explores how the Key-Value cache speeds up autoregressive generation by storing previously computed attention states instead of recomputing them.

Benefits:

* Faster generation
* Lower latency
* Reduced computation

### Continuous Batching

Instead of processing requests one by one, vLLM continuously schedules incoming requests to maximize GPU utilization.

Advantages:

* Higher throughput
* Better GPU efficiency
* Lower waiting time

### PagedAttention

One of the core innovations of vLLM.

Rather than allocating contiguous memory for every sequence, PagedAttention stores the KV cache in fixed-size memory blocks.

Benefits include:

* Efficient memory allocation
* Reduced fragmentation
* Higher concurrency
* Better scalability

### Prefix Caching

When multiple requests share the same prompt, vLLM reuses previously computed KV cache instead of recomputing the prefix.

Benefits:

* Reduced computation
* Lower latency
* Faster repeated prompts

---

## 📊 Benchmarking

Performance evaluation is performed using **GuideLLM**.

Metrics include:

* Requests per Second (RPS)
* Throughput
* Tokens per Second
* Latency
* Time To First Token (TTFT)
* GPU Utilization

---

## 📈 Model Evaluation

After quantization, the compressed model is evaluated using **lm-eval** to ensure quality remains close to the original model.

Evaluation focuses on:

* Perplexity
* Accuracy
* Language Understanding
* General Performance

---

## 🎓 Course

This project was completed as part of the **Fast & Efficient LLM Inference with vLLM** course by **DeepLearningAI** in partnership with **Red Hat**, focusing on modern techniques for optimizing and serving open-source Large Language Models.

---

## 👨‍💻 Author

**`Mohamed Fathy`**

Artificial Intelligence Engineer

Passionate about:

* Large Language Models
* AI & LLMs Infrastructure
* Model Optimization
* High-Performance AI Systems
* Generative AI

### ⭐ If you found this project helpful, consider giving it a star!?
