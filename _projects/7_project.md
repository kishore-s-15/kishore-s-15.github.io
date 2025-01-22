---
layout: page
title: Evolving Machine Unlearning
description: Benchmarking Privacy-Preserving Unlearning Methods on Real-World Facial Datasets
img: assets/img/projects/unlearning.png
importance: 7
category: academic
related_publications: false
---

### Overview

This project explores and benchmarks machine unlearning methods using the MUFAC facial dataset, demonstrating practical applications in privacy-preserving machine learning. The research implements and evaluates multiple unlearning approaches, with a particular focus on knowledge distillation-based techniques like SCRUB and gradient-based methods like NegGrad. The project also introduces a novel approach called MUNCHing (Machine Unlearning via Naive Checkpointing) that achieves superior performance in terms of both computational efficiency and unlearning effectiveness.

### Technical Implementation

The implementation centers around the MUFAC dataset, specifically tailored for multi-class facial age estimation across eight distinct categories. Our experimental framework utilizes ResNet-18 as the backbone architecture, chosen for its widespread adoption in machine unlearning research and its ability to facilitate comparative analysis against established benchmarks.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/unlearning_comparison.png' | relative_url }}" alt="Comparison of different unlearning methods" title="Performance comparison across unlearning methods"/>
    </div>
</div>
<div class="caption">
    Performance comparison showing accuracy retention and forgetting effectiveness across different unlearning methods
</div>

### Key Innovations

The project makes several significant contributions to the field of machine unlearning:

1. **MUNCHing Algorithm**: Developed a novel unlearning approach based on naive checkpoint approximations that achieves state-of-the-art performance in balancing computational efficiency and unlearning effectiveness.

2. **Comprehensive Evaluation Framework**: Engineered a robust privacy evaluation system incorporating three distinct Membership Inference Attack (MIA) approaches:
   - LiRA (Likelihood Ratio Attack)
   - Loss-based MIA
   - Classifier-based MIA

3. **Benchmarking Implementation**: Successfully implemented and benchmarked multiple existing approaches including SCRUB and NegGrad, achieving 88% retain set accuracy while reducing forget set accuracy to 66%.

### Privacy Evaluation Results

Our evaluation framework revealed interesting insights about the effectiveness of different unlearning methods:

- The LiRA attack achieved a 40.13% membership detection rate on baseline models
- MUNCHing demonstrated superior resistance to membership inference attacks compared to existing methods
- SCRUB and UNSIR showed high utility preservation but incomplete unlearning
- NegGrad achieved the best forgetting metrics but at a significant cost to utility

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/unlearning_metrics.png' | relative_url }}" alt="Privacy evaluation metrics" title="Privacy evaluation metrics across different methods"/>
    </div>
</div>
<div class="caption">
    Comparison of membership inference attack success rates and computational efficiency across different unlearning methods
</div>

### Impact and Future Work

This research contributes to the growing field of privacy-preserving machine learning by providing:

- A systematic comparison of existing unlearning methods
- A novel, efficient unlearning algorithm (MUNCHing)
- A comprehensive evaluation framework for assessing unlearning effectiveness
- Practical insights into the trade-offs between utility preservation and privacy protection

Future work includes expanding the evaluation to multiple datasets with different modalities and developing theoretical bounds for checkpoint estimation errors. The project is actively being developed into a Python library for benchmarking machine unlearning algorithms, scheduled for release in May 2025.   