---
title: "Assistive Vision - Android App"
excerpt: "TensorFlow-based mobile application for currency recognition and accessibility assistance."
tags:
  - Computer Vision
  - Mobile ML
  - TensorFlow Lite
  - Android
  - Accessibility
date: 2024-11-01
github: https://github.com/shubhamgogri/Assistive-Vission
---

## Overview

An Android application designed to assist visually impaired users by providing real-time currency recognition, cloth pattern identification, and text-to-speech capabilities.

## Features

**Currency Recognition**
- Predicts Indian currency denominations with 85% accuracy
- Uses pre-trained EfficientDet-Lite0 model optimized for mobile
- TensorFlow Lite integration for on-device inference

**Cloth Pattern Recognition**
- Identifies cloth patterns with 76% accuracy
- Helps users distinguish between different fabric types

**Accessibility Features**
- Google Text-to-Speech API integration for audio feedback
- ML-Kit Object Detection for general object identification
- Handwritten Text Recognition for reading documents

## Technical Implementation

- **Model:** EfficientDet-Lite0 fine-tuned for currency classification
- **Platform:** Android with TensorFlow Lite
- **APIs:** ML-Kit, Google Text-to-Speech
- **Optimization:** Model quantization for mobile deployment

## Impact

- Published research in Dickensian Journal documenting the approach
- Demonstrates practical application of ML for accessibility
- End-to-end mobile ML pipeline from training to deployment

## Tech Stack

`TensorFlow` `TensorFlow Lite` `Android` `ML-Kit` `EfficientDet` `Java` `Python`

## Links

- [GitHub Repository](https://github.com/shubhamgogri/Assistive-Vission)
