---
layout: page
title: Deep Leaf
description: Deep Learning for Plant Disease Classification
img: assets/img/projects/plant_pathology.png
importance: 6
category: personal
related_publications: false
---

### Overview

Deep Leaf is a sophisticated deep learning project focused on automating plant disease diagnosis through leaf image analysis. The system leverages state-of-the-art neural network architectures including DenseNet121 and EfficientNet models, incorporating advanced techniques such as weighted loss functions and ensemble methods to achieve robust disease classification accuracy of up to 97%.

### Architecture and Implementation

The project implements multiple deep learning models and ensemble techniques to maximize classification accuracy across different plant diseases. At its core, the system utilizes three primary architectures:

- **DenseNet121**: Features dense connectivity patterns that strengthen feature propagation and encourage feature reuse
- **EfficientNetB1**: Employs compound scaling to optimize the balance between network depth, width, and resolution
- **EfficientNetB2**: Enhances the base EfficientNet architecture with progressive learning and fine-tuned compound coefficients

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/DenseNet-architecture.png' | relative_url }}" alt="DenseNet Architecture" title="DenseNet Architecture"/>
    </div>
</div>
<div class="caption">
    DenseNet architecture showing dense connectivity pattern between layers
</div>

### Data Processing and Augmentation

The system processes a comprehensive dataset of plant leaf images, categorized into four distinct classes: Healthy, Multiple Diseases, Rust, and Scab. The data pipeline includes:

1. **Image Preprocessing**: 
   - Standardization to 512x512 pixels
   - Normalization of pixel values
   - Implementation of various augmentation techniques including random flips, rotations, and color adjustments

2. **Class Distribution Handling**:
   - Strategic data splitting (70% training, 20% validation, 10% test)
   - Implementation of weighted loss functions to address class imbalance
   - Monitoring of batch-level class distribution

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/batch_visualization.png' | relative_url }}" alt="Batch Visualization Example" title="Batch Visualization Example"/>
    </div>
</div>
<div class="caption">
    Visualization of processed and augmented training batch samples
</div>

### Model Performance and Ensemble Methods

The project implements two sophisticated ensemble approaches to maximize classification accuracy:

1. **Average Ensemble**:
   - Combines predictions from all three models through probability averaging
   - Achieves 96% accuracy with enhanced robustness across classes

2. **Soft Voting Ensemble**:
   - Weights model predictions based on confidence levels
   - Reaches 97% accuracy with improved performance on challenging cases

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/softvoting_ensambling_confusion_matrix.png' | relative_url }}" alt="Soft Voting Ensemble Confusion Matrix" title="Soft Voting Ensemble Performance"/>
    </div>
</div>
<div class="caption">
    Confusion matrix showing the superior performance of the soft voting ensemble method
</div>

### Model Interpretability

To ensure transparency and validate the model's decision-making process, the project incorporates Grad-CAM visualizations, providing insight into the regions of interest that influence classification decisions.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/grad-cam-viz_1.png' | relative_url }}" alt="Grad-CAM Visualization" title="Grad-CAM Analysis"/>
    </div>
</div>
<div class="caption">
    Grad-CAM visualization highlighting regions of interest in disease classification
</div>

### Technical Achievements

The project demonstrates several key technical accomplishments:

- Implementation of weighted loss functions to address class imbalance
- Achievement of 97% accuracy through ensemble methods
- Development of interpretable AI through Grad-CAM visualizations
- Successful handling of multi-class disease classification
- Robust performance across varied disease presentations