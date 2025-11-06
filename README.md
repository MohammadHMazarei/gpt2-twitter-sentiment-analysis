# GPT2 Twitter Sentiment Analysis

Fine-tuning GPT2 for sentiment classification on Twitter data using the MTEB Tweet Sentiment Extraction dataset.

## 📋 Overview

This project fine-tunes OpenAI's GPT2 model for sentiment analysis on tweets. The model classifies tweets into three sentiment categories using the `mteb/tweet_sentiment_extraction` dataset from Hugging Face.

## 🚀 Features

- Fine-tuned GPT2 model for sequence classification
- Three-class sentiment classification (positive, negative, neutral)
- Training monitoring with Weights & Biases (wandb)
- Efficient training with gradient accumulation

## 📊 Dataset

- **Source**: [MTEB Tweet Sentiment Extraction](https://huggingface.co/datasets/mteb/tweet_sentiment_extraction)
- **Task**: Sentiment Classification
- **Classes**: 3 (positive, negative, neutral)
- **Training samples used**: 1,000 (small dataset for quick experimentation)
- **Test samples used**: 1,000

## 📈 Training Configuration

Parameter | Value
--- | ---
Base Model | GPT2
Number of Labels | 3
Train Batch Size | 1
Eval Batch Size | 1
Gradient Accumulation Steps | 4
ffective Batch Size | 4

## 🔍 Model Architecture

- **Base Model**: GPT2 (124M parameters)
- **Classification Head**: Linear layer for 3-class classification
- **Tokenizer**: GPT2 tokenizer with EOS token as padding token
