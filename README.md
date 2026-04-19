# Multimodal Deep Learning for Melanoma Diagnosis and Malignancy Grading

This repository contains the official implementation of the paper:

**"Deep Multimodal Fusion of Dermoscopic Images and Structured Pathological Reports for High-Accuracy Melanoma Diagnosis and Prognostic Grading"** 

## Overview

This project develops a multimodal deep learning system for:
1. **Binary classification** - Melanoma vs. non-melanoma from dermoscopy images
2. **Four-class malignancy grading** (Grades 0-3) using dermoscopy + pathology features

## Architecture

- **Image branch**: DenseNet201, Xception, or InceptionV3 (pretrained on ImageNet)
- **Pathology branch**: 4 features (Breslow thickness, Clark level, Ulceration, Mitotic rate) → Dense(64)
- **Fusion**: Late concatenation (2,112-dim vector) → Dense(256) → Dense(128) → Softmax(4)
