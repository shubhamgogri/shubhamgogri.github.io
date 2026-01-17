---
title: "Deep Learning for Image Correction in Sparse-View CT"
excerpt: "GAN-based medical imaging reducing X-ray dosage. Published at ICMLMI 2023, nominated for Best Dissertation Award."
tags:
  - Computer Vision
  - GANs
  - Medical Imaging
  - TensorFlow
  - Research
date: 2024-12-01
github: https://github.com/shubhamgogri/Image_Correction_in_SparseView_CT
publication: https://publications.waset.org/abstracts/172152/deep-learning-for-image-correction-in-sparse-view-
---

## Overview

My MSc dissertation project focused on reducing radiation exposure in CT scans through deep learning-based image reconstruction. Medical diagnosis and radiotherapy treatment planning rely on the quantitative accuracy and quality of CT images, but reducing radiation dose and scanning time is critical for patient safety. Sparse-view CT—using fewer projection views—offers a solution, but introduces image quality degradation. This research applied deep learning to enhance sparse-view CT image quality.

## The Problem

Computed Tomography (CT) imaging requires balancing two competing requirements: high image quality for accurate diagnosis, and minimizing radiation exposure to patients. Sparse-view CT reduces radiation by using fewer X-ray projections, but the incomplete projection data results in severe artifacts and lower image quality. The challenge: can deep learning reconstruct clinically usable images from sparse inputs?

## Approach

### Phase 1: MIR-Net Baseline
Initial experiments employed MIR-Net, a dedicated deep neural network designed for image enhancement. The architecture comprised encoder and decoder networks with Charbonnier Loss for optimization. While promising, this approach proved computationally demanding.

### Phase 2: Pix2Pix GAN Architecture
A specialized GAN architecture rooted in the Pix2Pix framework was implemented:

**Generator:** U-Net-based architecture for image-to-image translation
**Discriminator:** Convolutional Neural Network for adversarial training

**Loss Functions (Key Innovation):**
- **Charbonnier Loss:** Captures minute details in reconstruction
- **Wasserstein Loss:** Ensures training stability
- **Perceptual Loss:** Calculated from VGG16 feature vectors (pretrained on ImageNet) to enhance synthesis of visually relevant images

### Training Infrastructure
- Containerized training pipelines using Docker
- Deployed on University of Surrey's HPC cluster (Condor system)
- Comprehensive experiments with clinical CT data
- Systematic exploration of loss function combinations

## Results

The experiments demonstrated significant image quality improvements:

| Metric | Performance |
|--------|-------------|
| **SSIM** | Values approaching 1.0 (near-perfect structural similarity) |
| **PSNR** | Up to 76 dB (excellent signal-to-noise ratio) |

Additional findings:
- Learning curves demonstrated enhanced training stability
- Qualitative comparisons confirmed improved visual interpretation
- Pixel value intensity preserved during reconstruction
- GAN-based approaches significantly outperformed traditional methods

## Recognition

- **Best Dissertation Nomination** — University of Surrey, Electronic Engineering Industrial Advisory Board (2023-24)
- **Publication** — Abstract accepted at ICMLMI 2023 (International Conference on Machine Learning in Medical Imaging), London

## What I Learned

This project shaped how I think about applied ML research:

**Technical insights:**
- Loss function design is as important as architecture design
- Perceptual loss (VGG16 features) dramatically improves visual quality
- Combining multiple loss functions requires careful balancing

**Research methodology:**
- Containerization enables reproducible experimentation at scale
- Systematic comparison across configurations reveals what actually works
- Quantitative metrics (PSNR, SSIM) must be paired with qualitative assessment

## Tech Stack

`TensorFlow` `Pix2Pix GAN` `U-Net` `MIR-Net` `VGG16` `Docker` `HPC/Condor` `Python` `OpenCV` `NumPy`

## Resources

- [View Presentation (PDF)](/assets/documents/sparse-ct-presentation.pdf) — Overview presented at ICMLMI 2023
- [Full Dissertation (PDF)](/assets/documents/sparse-ct-dissertation.pdf) — Complete research report with methodology and results
- [GitHub Repository](https://github.com/shubhamgogri/Image_Correction_in_SparseView_CT)
- [ICMLMI Publication Abstract](https://publications.waset.org/abstracts/172152/deep-learning-for-image-correction-in-sparse-view-)
