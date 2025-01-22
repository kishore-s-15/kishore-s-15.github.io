---
layout: page
title: Pencil2Pixel
description: Enhancing Forensic Sketch-to-Image Generation with Advanced Preprocessing
img: assets/img/projects/pencil2pixel.webp
importance: 4
category: personal
related_publications: false
---

### Overview

Pencil2Pixel presents an innovative approach to forensic sketch-to-image generation using Generative Adversarial Networks (GANs) with advanced preprocessing techniques. The system demonstrates significant improvements in image quality through gamma inversion preprocessing, achieving SSIM scores up to 0.8076 and PSNR values up to 23.015, compared to baseline scores of 0.7025 and 18.40 respectively. This project introduces a dual-phase training approach where GANs are first trained with standard sketches and then re-trained with gamma-inverted sketches, showing marked improvements in visual quality.

### Architecture

The system implements a dual-architecture approach with a U-Net Generator and PatchGAN Discriminator, designed to optimize both feature extraction and image generation quality. The U-Net Generator provides progressive feature compression and expansion through encoder-decoder paths with skip connections, while the PatchGAN Discriminator employs five convolutional layers for enhanced local feature discrimination.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/gan_architecture.png' | relative_url }}" alt="Complete system architecture showing generator and discriminator components" title="Complete system architecture showing generator and discriminator components"/>
    </div>
</div>
<div class="caption">
    Complete system architecture showing U-Net Generator and PatchGAN Discriminator architectures with preprocessing pipeline
</div>

### Base Architecture and Processing Pipeline

The system utilizes a comprehensive processing pipeline that includes:
- Gamma inversion preprocessing for enhanced sketch quality
- U-Net Generator with progressive feature compression/expansion
- PatchGAN Discriminator with batch normalization and LeakyReLU activation
- Skip connections between corresponding encoder and decoder layers
- Patch-based output for local feature discrimination

### Feature Enhancement and Training Process

The training process implements several sophisticated components:
- Separate Adam optimizers for generator and discriminator
- Combined adversarial and L1 losses for improved training stability
- Regular evaluation using L1 loss on validation set
- Early stopping mechanisms to prevent overfitting
- Systematic grid search for optimal hyperparameter tuning

### Technical Implementation

The model implementation includes several key technical components:

- **Generator Architecture**: Encoder-decoder path with skip connections
- **Discriminator Design**: Five-layer convolutional network with progressive downsampling
- **Preprocessing Pipeline**: Gamma inversion and image enhancement techniques
- **Training Strategy**: Dual-phase approach with alternating discriminator and generator updates

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/training_pipeline.png' | relative_url }}" alt="Training pipeline showing preprocessing and model components" title="Training pipeline showing preprocessing and model components"/>
    </div>
</div>
<div class="caption">
    Training pipeline showing preprocessing steps, model components, and evaluation metrics
</div>

### Performance Evaluation

The system demonstrates significant improvements across key metrics:

- **SSIM Score**: Improved from 0.7025 (baseline) to 0.8076 (+15.0%)
- **PSNR Value**: Enhanced from 18.40 to 23.015 (+25.1%)
- **Grid Search Results**: Optimal performance achieved with learning rate of 0.005, batch size of 8, and dropout rate of 0.1
- **Training Stability**: Consistent convergence across multiple runs with early stopping

The model was extensively evaluated through grid search over various hyperparameters including learning rates [0.0002, 0.0005, 0.001, 0.005], batch sizes [8, 16, 32, 64], and dropout rates [0.1, 0.3, 0.5], utilizing combined loss functions for optimization.