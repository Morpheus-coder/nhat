<h1 align="center">🧠 Morpheus AI</h1>
<p align="center">
  <strong>Mental Health Early Detection & Support System</strong><br>
  <em>AI-powered text analysis for mental health awareness</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?logo=python" />
  <img src="https://img.shields.io/badge/PyTorch-2.0+-red?logo=pytorch" />
  <img src="https://img.shields.io/badge/HuggingFace-Transformers-yellow?logo=huggingface" />
  <img src="https://img.shields.io/badge/Gradio-4.0+-orange?logo=gradio" />
  <img src="https://img.shields.io/badge/License-MIT-green" />
</p>

---

## 📋 Overview

**Morpheus AI** uses Natural Language Processing (NLP) to analyse text and detect early signs of mental health conditions. Named after the god of dreams and the awakener from The Matrix, Morpheus AI aims to **awaken awareness** about mental health.

### 🎯 Classification Categories

| Category | Description | Severity |
|----------|-------------|----------|
| 🟢 **Normal** | No significant mental health indicators | Low |
| 🟡 **Anxiety** | Signs of anxiety or excessive worry | Medium |
| 🟠 **Depression** | Indicators of depressive states | High |
| 🔴 **Suicidal** | Expressions of suicidal ideation | Critical |

### ✨ Features

- **Text Analysis** — Classify text into 4 mental health categories with confidence scores
- **Support Chatbot** — Empathetic AI companion powered by LLM
- **Crisis Resources** — Immediate access to hotlines and support services
- **Beautiful UI** — Dark-themed, Matrix-inspired Gradio interface

---

## 🚀 Quick Start

### Prerequisites

- Python 3.10+
- NVIDIA GPU with CUDA (recommended: RTX 3050Ti or better)
- ~4GB disk space for model & data

### Installation

```bash
# Clone the repository
git clone https://github.com/your-username/morpheus-ai.git
cd morpheus-ai

# Create virtual environment
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # Linux/Mac

# Install dependencies
pip install -r requirements.txt
```

### Training

```bash
# Train with default settings (5 epochs, BERT-base)
python train.py

# Custom training
python train.py --epochs 10 --batch-size 16 --lr 3e-5
```

### Inference (CLI)

```bash
python predict.py "I feel so hopeless and empty inside"
```

### Web Application

```bash
python app/app.py
# Open http://localhost:7860
```

---

## 📁 Project Structure

```
morpheus-ai/
├── src/
│   ├── config.py          # All configuration & hyperparameters
│   ├── data_loader.py     # Dataset loading & preprocessing
│   ├── model.py           # BERT classifier wrapper
│   ├── trainer.py         # HuggingFace Trainer integration
│   ├── predictor.py       # Inference engine
│   └── utils.py           # Metrics & visualisation
├── app/
│   └── app.py             # Gradio web application
├── data/                  # Datasets (auto-downloaded)
├── models/                # Saved checkpoints
├── logs/                  # TensorBoard logs & plots
├── train.py               # Training entry point
├── predict.py             # CLI prediction
├── requirements.txt
└── README.md
```

---

## 📊 Model Architecture

- **Base Model**: `bert-base-uncased` (110M parameters)
- **Task**: Multi-class sequence classification (4 classes)
- **Dataset**: [Mental Health Text Classification](https://huggingface.co/datasets/ourafla/Mental-Health_Text-Classification_Dataset) (~51k samples)
- **Training**: Fine-tuning with class-weighted loss, FP16 mixed precision, early stopping

---

## ☁️ Deploy to Hugging Face Spaces

```bash
# 1. Login to HuggingFace
huggingface-cli login

# 2. Create a Space and push
# (Follow HuggingFace Spaces documentation)
```

---

## ⚠️ Disclaimer

> **Morpheus AI is NOT a medical diagnostic tool.**
> It is designed for informational and awareness purposes only.
> Always consult qualified mental health professionals for diagnosis and treatment.
>
> **If you are in crisis:**
> - 🇻🇳 Vietnam: **1800 599 920** (24/7)
> - 🇺🇸 US: **988** Suicide & Crisis Lifeline
> - 🌍 Crisis Text Line: Text **HOME** to **741741**

---

## 📄 License

This project is licensed under the MIT License.

---

<p align="center">Built with 💙 for mental health awareness</p>
