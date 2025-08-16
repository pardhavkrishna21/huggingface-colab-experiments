Hugging Face + Google Colab Experiments 🚀

This repo contains my experiments with Hugging Face pipelines using Google Colab.

✨ Tasks Covered

✅ Sentiment Analysis

✅ Question Answering with Context

✅ Named Entity Recognition (NER)

✅ Text Summarization

✅ Translation

✅ Classification (Zero-Shot, etc.)

✅ Text Generation

✅ Text-to-Audio (Speech Synthesis)

▶️ Usage in Colab

In Google Colab, just run the following in a cell:

!pip install -q transformers datasets diffusers sentencepiece soundfile


Then you can import and use Hugging Face pipelines, e.g.:

from transformers import pipeline

classifier = pipeline("sentiment-analysis")
print(classifier("I love experimenting with Hugging Face on Colab!"))

📂 Structure

notebooks/ → Contains all Google Colab notebooks with experiments

README.md → Project documentation
