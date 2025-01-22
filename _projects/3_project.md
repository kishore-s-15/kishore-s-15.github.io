---
layout: page
title: MemeSense
description: A Multimodal Framework for Meme Analysis using Enhanced CLIP
img: assets/img/projects/meme_sense.png
importance: 3
category: personal
related_publications: false
---

### Overview

MemeSense is a sophisticated multimodal framework that leverages OpenAI's CLIP architecture for comprehensive meme analysis. The system combines feature adapters and cosine classifiers with a semantic-aware initialization strategy to achieve high-performance classification across multiple tasks. By implementing a multi-modal architecture with enhanced CLIP features, the system effectively processes both visual and textual components of memes to perform tasks such as humor detection, hate speech identification, target classification, and stance analysis.

### Architecture

The MemeSense framework is built upon a multi-component architecture designed to process both visual and textual elements of memes through specialized modules. Its core implementation uses CLIP's pre-trained knowledge combined with custom feature adapters and a semantic-aware initialization strategy. This design enables efficient processing of multimodal content while maintaining the rich pre-trained knowledge of the CLIP model.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/memeclip_architecture.png' | relative_url }}" alt="Complete system architecture of MemeSense" title="Complete system architecture of MemeSense"/>
    </div>
</div>
<div class="caption">
    Complete system architecture showing CLIP encoders, feature adapters, and classification components
</div>

### Base Architecture and Feature Processing

The system utilizes CLIP's Vision Transformer (ViT-L/14) for processing images and a text encoder for handling textual content. The vision encoder processes 224x224 RGB images through 24 transformer layers, while the text encoder handles up to 77 tokens through 12 transformer layers. Both encoders output 768-dimensional feature vectors that capture rich semantic information from their respective modalities. These base encoders are kept frozen to preserve CLIP's pre-trained knowledge while additional components are trained for task-specific optimization.

### Feature Adaptation and Enhancement

Building on the base architecture, MemeSense implements a sophisticated feature adaptation mechanism. The system first projects the initial 768-dimensional features to a higher 1024-dimensional space using configurable linear projection layers. These projected features then pass through specialized adapter modules that modify them for specific tasks while maintaining a connection to the original features through residual integration. The adapter modules implement a bottleneck architecture, reducing the feature dimension by a factor of 4 before restoration, allowing for efficient task-specific adaptations.

### Semantic-Aware Classification

The classification mechanism employs a novel semantic-aware initialization strategy that leverages CLIP's pre-trained understanding of concepts. This approach initializes classifier weights using CLIP's semantic knowledge of the target classes, creating more meaningful decision boundaries from the start. The classification process uses cosine similarity with temperature scaling, allowing the model to make confident predictions while maintaining semantic relationships between features and class representations.

### Technical Implementation

The complete model comprises 3,675,136 parameters and implements several key technical components:

- **Feature Projection**: Configurable depth projection layers that map CLIP features to higher dimensions
- **Adapter Modules**: Bottleneck architecture for task-specific feature adaptation
- **Residual Integration**: Weighted combination of adapted and projected features (0.2:0.8 ratio)
- **Cosine Classification**: Temperature-scaled (30) cosine similarity for final predictions

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/meme_training.png' | relative_url }}" alt="MemeSense Training Process" title="MemeSense Training Process"/>
    </div>
</div>
<div class="caption">
    Training pipeline showing data processing, feature extraction, and classification components
</div>

### Performance Evaluation

The system demonstrates strong performance across multiple classification tasks:

- **Humor Recognition**: 80.27% accuracy with 85.59% AUC
- **Hate Speech Detection**: 76.06% accuracy with 84.52% AUC
- **Target Identification**: 66.12% accuracy with 81.66% AUC
- **Stance Classification**: 62.00% accuracy with 80.11% AUC

The model was trained on the PrideMM dataset comprising 5,063 annotated memes, with 4,666 samples for training and 397 for validation. Training utilized a batch size of 16, learning rate of 1e-4, and weight decay of 1e-4 over 10 epochs, employing Cross Entropy Loss with mean reduction for optimization.