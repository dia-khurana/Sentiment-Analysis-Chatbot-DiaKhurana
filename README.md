# Sentiment-Analysis-Chatbot-DiaKhurana
## 1. Introduction

This repository contains a sentiment analysis chatbot developed as a submission for a pre-placement evaluation task. The chatbot classifies user text input into positive or negative sentiment using a pre-trained DistilBERT model. It integrates basic rule-based logic for handling greetings, exit commands, and sentiment-based responses, wrapped within an interactive Gradio web interface to demonstrate real-time usage.

The objective is to showcase the ability to work with transformer models, perform inference, and combine model outputs with application-level control flow to build a functional chatbot prototype.

## 2. Technology Stack

- Python 3.8+
- HuggingFace Transformers library
- PyTorch for deep learning inference
- Gradio for web UI interfacing

## 3. Solution Architecture

User messages are handled with the following pipeline:

1. Input text is tokenized using the DistilBERT tokenizer.
2. Tokenized input is passed to the DistilBERT model fine-tuned on SST-2 sentiment dataset.
3. Model outputs logits that are converted to probabilities using softmax.
4. Sentiments are determined by comparing positive and negative scores.
5. Rule-based system decides responses for greetings, exits, or based on sentiment label.
6. Responses along with sentiment scores are displayed in a chat interface managed by Gradio.
