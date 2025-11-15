# CURL: Neural Curve Layers for Global Image Enhancement

This repository contains the official PyTorch implementation for the paper, "CURL: Neural Curve Layers for Global Image Enhancement," presented at the International Conference on Pattern Recognition (ICPR) 2020.

CURL introduces a novel, end-to-end deep learning approach to adaptive photo retouching, inspired by professional curve adjustment tools (like Photoshop Curves).

### Core Architecture: $\text{TED+CURL}$

The project implements a two-stage pipeline for image enhancement:

$\text{TED}$ (Transformed Encoder-Decoder): The backbone network responsible for local pixel-level feature extraction (denoising, demosaicing) and collecting multi-scale contextual awareness ($\text{MSCA}$) features.

$\text{CURL}$ (Neural CURve Layers): A pluggable neural block that predicts a set of piecewise-linear scaling curves to apply global, image-adaptive tonal and chromatic adjustments across three distinct color spaces ($\text{CIELab} \to \text{RGB} \to \text{HSV}$).

### Key Features

Multi-Color Space Enhancement: Adjustments are learned jointly across $\text{CIELab}$, $\text{RGB}$, and $\text{HSV}$ spaces, guided by a specialized loss function ($\mathcal{L}_{\text{total}}$).

Arbitrary Resolution Support: The architecture uses Adaptive Global Pooling to ensure the model can process input images of any size.

Original Code: https://github.com/sjmoran/curl-image-enhancement

Official IEEE Xplore link to the publication: https://ieeexplore.ieee.org/document/9412677
