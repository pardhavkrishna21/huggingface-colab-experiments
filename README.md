🤗 Hugging Face + Google Colab Experiments 🚀

This repository contains my experiments with Hugging Face using Google Colab.
I explore both pipelines (high-level API for inference) and tokenizers (low-level text preprocessing API) across a variety of NLP and generative tasks.

📂 Notebooks
1️⃣ ner_classification_tts.ipynb — Hugging Face Pipelines

This notebook demonstrates the pipeline API, which allows quick access to pre-trained models for common tasks.

✨ Tasks Covered:

✅ Sentiment Analysis

✅ Question Answering with Context

✅ Named Entity Recognition (NER)

✅ Text Summarization

✅ Translation

✅ Classification (Zero-Shot, etc.)

✅ Text Generation

✅ Text-to-Audio (Speech Synthesis)

2️⃣ tokenizers.ipynb — Exploring Tokenizers
▶️ Usage Example

!pip install -q transformers datasets diffusers sentencepiece soundfile

from transformers import pipeline

classifier = pipeline("sentiment-analysis")
print(classifier("I love experimenting with Hugging Face on Colab!"))

This notebook explores tokenization with Hugging Face and demonstrates how different LLM tokenizers behave.

📖 Key Topics:

Setting up Colab with PyTorch + Transformers.

Authenticating with Hugging Face API token.

Accessing gated models like Meta-LLaMA 3.1-8B (after requesting access).

Tokenization basics: encode, decode, batch_decode, and vocab lookups.

Working with Instruct model variants using apply_chat_template.

Comparing tokenizers from multiple LLMs:

Meta-LLaMA 3.1

Microsoft Phi-3

Qwen2

Starcoder2
setup:
!pip install -q --upgrade torch==2.5.1+cu124 torchvision==0.20.1+cu124 torchaudio==2.5.1+cu124 --index-url https://download.pytorch.org/whl/cu124
!pip install -q --upgrade transformers==4.48.3 datasets==3.2.0

🔑 Authentication
from google.colab import userdata
from huggingface_hub import login
hf_token = userdata.get("HF_TOKEN")
login(hf_token, add_to_git_credential=True)
