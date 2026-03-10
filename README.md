# EmeiTourBench (ETB) 🏔️

**EmeiTourBench: A Multi-Source Benchmark for Evaluating Large Language Models in Authentic Chinese Tourism Scenarios**

[![License](https://img.shields.io/badge/License-Apache--2.0-blue.svg)](LICENSE)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-green.svg)](https://www.python.org/downloads/)

---

## 🌟 Overview
**EmeiTourBench (ETB)** is a large-scale, multi-source Chinese tourism QA benchmark designed to evaluate the robustness of Large Language Models (LLMs) in real-world vertical domains. 

By integrating five heterogeneous data channels, ETB captures the **distribution shifts** and linguistic complexities inherent in authentic service scenarios—ranging from normative official documents to noisy, spontaneous hotline transcripts.



## 📊 Dataset Statistics
The benchmark comprises **29,641** refined records, categorized by their source and task type:

| Source Slice | Count | Category | Feature |
| :--- | :--- | :--- | :--- |
| **Official Doc** | 17,684 | Factual / Reasoning | Normative texts with context grounding |
| **Hotline** | 11,372 | Spontaneous | Multi-turn dialogues with ASR noise |
| **RedNote** | 449 | Social Media | Long-tail user-generated content |
| **FAQ** | 108 | Factual | High-frequency official queries |
| **Dist** | 28 | Navigation | Spatial-numerical reasoning |
| **Total** | **29,641** | - | - |

## 🛡️ Quality Control: The CAT Framework
To ensure the rigor of synthetic data, we propose the **CAT framework**, focusing on three dimensions:
* **Coherence (Coh)**: Ensures logical consistency between questions and answers.
* **Accuracy (Acc)**: Guarantees strict alignment with the provided source context.
* **Traceability (Tra)**: Ensures that all generated answers can be traced back to verifiable evidence.



## 🛠️ Data Format
Records are provided in a standardized JSON format to facilitate seamless evaluation:

```json
{
  "id": "ETB-Hotline-Multi-00458",
  "source": "Hotline",
  "category": "Spontaneous",
  "dialogue": [
    { "游客": "索道缆车能直达金顶吗？", "客服": "到雷洞坪后要走半小时路才能坐索道上山。" }
  ],
  "question": "老人坐索道有优惠吗？",
  "answer": "老人坐索道没有优惠。",
  "metadata": {
    "is_multi_turn": true,
    "has_context": false
  }
}
