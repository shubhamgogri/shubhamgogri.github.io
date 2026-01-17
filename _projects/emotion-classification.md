---
title: "Emotion Classification Pipeline"
excerpt: "27-class emotion recognition using DistilBERT, Bi-LSTM, and CNN-LSTM. Deployed on HuggingFace Spaces."
tags:
  - NLP
  - Deep Learning
  - Classification
  - MLOps
  - Deployment
date: 2023-11-01
github: https://github.com/shubhamgogri/EmotionClassification
demo: https://huggingface.co/spaces/shubhamgogri/emotion-classification
---

## Overview

A multi-class text classification system identifying 27 distinct emotions in text, trained on the GoEmotions dataset of Reddit comments. This project explored multiple deep learning architectures and culminated in a deployed web application.

## The Problem

Fine-grained emotion recognition is challenging—distinguishing between 27 emotional states (not just positive/negative sentiment) requires nuanced understanding of language. The GoEmotions dataset provides 197,847 labeled Reddit comments across these categories.

## Approach

**Experimentation:**
Conducted systematic experiments comparing multiple architectures:

| Model | Architecture | Test Accuracy |
|-------|--------------|---------------|
| Baseline | N-Gram + Traditional ML | 39.58% |
| Bi-LSTM | Bidirectional LSTM | 59.26% |
| CNN-LSTM | Convolutional + LSTM hybrid | 41.09% |
| DistilBERT | Transformer-based | Competitive |

**Key Techniques:**
- Preprocessing and N-Gram analysis for baseline
- Bidirectional LSTM for capturing context in both directions
- CNN-LSTM hybrid combining local feature extraction with sequence modeling
- Hyperparameter tuning across architectures

**MLOps & Deployment:**
- Model tracking with Weights & Biases (wandb)
- Web application built with Gradio
- Deployed on HuggingFace Spaces
- CI/CD pipeline for continuous deployment

## Results

- Bi-LSTM achieved best performance at 59.26% accuracy on 27-class problem
- Demonstrated that sequence models capture emotional nuance better than bag-of-words approaches
- Successfully deployed interactive demo for real-time inference

## What I Learned

This project reinforced the importance of:
- Systematic experimentation with proper tracking (W&B)
- The value of deploying models—a live demo communicates impact better than metrics alone
- Trade-offs between model complexity and performance
- CI/CD practices for ML applications

## Tech Stack

`TensorFlow` `DistilBERT` `Bi-LSTM` `Weights & Biases` `Gradio` `HuggingFace Spaces` `Python`

## Links

- [GitHub Repository](https://github.com/shubhamgogri/EmotionClassification)
- [Live Demo on HuggingFace](https://huggingface.co/spaces/shubhamgogri/emotion-classification)
