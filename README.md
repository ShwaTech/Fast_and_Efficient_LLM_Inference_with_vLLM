# 🚀 Fast & Efficient LLM Inference with vLLM

> Optimize, deploy, and benchmark Large Language Models using LLM Compressor, vLLM, GuideLLM, and lm-eval.

![Python](https://img.shields.io/badge/Python-3.11+-blue?style=for-the-badge\&logo=python)
![vLLM](https://img.shields.io/badge/vLLM-LLM%20Serving-green?style=for-the-badge)
![LLM](https://img.shields.io/badge/LLM-Inference-orange?style=for-the-badge)
![AI](https://img.shields.io/badge/Artificial-Intelligence-red?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-success?style=for-the-badge)

## Create a Conda Environment and  Install The Requirements

```bash
# Create Conda Evnironment
conda create -n "LLM-Inference-env" python=3.11 -y

# Activate Conda Evnironment
conda activate LLM-Inference-env

# Install The Requirements
pip install -r requirements.txt
```

---

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
| Groq API       | Client Interface             |

---
