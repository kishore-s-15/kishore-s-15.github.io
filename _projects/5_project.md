---
layout: page
title: Cricshot Prediction
description: AI-Powered Cricket Shot Classification & Similarity Analysis
img: assets/img/projects/cricket_shot.png
importance: 5
category: personal
related_publications: false
---

### Overview

Cricshot Prediction is an innovative deep learning system designed to analyze and classify cricket batting shots from video footage. By leveraging advanced CNN-GRU architecture and genetic algorithm-based optimization, the system achieves high accuracy in shot classification while also providing unique insights into shot similarities. This project demonstrates the practical application of AI in sports analytics, particularly in cricket coaching and player development.

### Architecture

The system employs a sophisticated hybrid architecture that combines Convolutional Neural Networks (CNN) with Gated Recurrent Units (GRU) to process both spatial and temporal features of cricket shots. The EfficientNet family serves as the backbone for feature extraction, while GRU units capture the temporal dynamics of batting movements.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/cricket_model_arch.png' | relative_url }}" alt="Model architecture showing CNN-GRU integration" title="Model Architecture"/>
    </div>
</div>
<div class="caption">
    Complete model architecture showing the CNN-GRU integration for temporal-spatial feature processing
</div>

### Dataset Preparation & Enhancement

The project utilizes the CrickShot10 dataset as its foundation, with several key enhancements to improve model robustness:
- Removal of score overlay text to focus on pure shot mechanics
- Implementation of horizontal flips to account for left and right-handed batting styles
- Strategic dataset splitting (70-20-10) for comprehensive model evaluation
- Temporal sampling of 30 frames per video to capture complete shot execution

### Model Variants & Performance

Three distinct model variants were developed and evaluated, each utilizing a different EfficientNet backbone:

| Model | Test Accuracy | Precision | Recall | F1 Score |
|-------|---------------|-----------|---------|-----------|
| EfficientNetB0 | 94% | 94% | 94% | 94% |
| EfficientNetV2B0 | 81% | 82% | 81% | 81% |
| EfficientNetB4 | 74% | 75% | 74% | 74% |

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/genetic_algo.png' | relative_url }}" alt="Genetic Algorithm Optimization Process" title="Hyperparameter Optimization"/>
    </div>
</div>
<div class="caption">
    Genetic algorithm-based hyperparameter optimization process and convergence
</div>

### Hyperparameter Optimization

A genetic algorithm-based approach was implemented for hyperparameter tuning, featuring:
- Population-based exploration of learning rates (0.0001-0.02) and epochs (1-20)
- Fitness evaluation based on validation accuracy
- Tournament selection for parent chromosomes
- Adaptive mutation rates to balance exploration and exploitation
- Stagnation limit of 10 generations for efficient convergence

### Shot Similarity Analysis

The project introduces a novel approach to analyzing similarities between different cricket shots:
- Feature extraction from the EfficientNet backbone's convolutional layers
- Vector representation of shot characteristics
- Cosine similarity computation between shot vectors
- Validation through identical video comparison (100% similarity baseline)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/shot_similarity.png' | relative_url }}" alt="Shot Similarity Analysis" title="Shot Similarity Matrix"/>
    </div>
</div>
<div class="caption">
    Shot similarity matrix showing relationships between different cricket shots
</div>

### Technical Implementation

The system leverages several key technologies and frameworks:
- TensorFlow for model development and training
- EfficientNet architectures for feature extraction
- GRU units for temporal sequence processing
- Custom genetic algorithm implementation for hyperparameter optimization
- Streamlit for web interface development