---
layout: page
permalink: /projects/
title: projects
description: My technical projects and research work
nav: true
nav_order: 4
---

<style>
.projects-container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
    margin-top: 1.5rem;
}

.project-card {
    background: var(--global-bg-color);
    border-radius: 12px;
    overflow: hidden;
    transition: transform 0.3s ease, box-shadow 0.3s ease;
    border: 1px solid var(--global-divider-color);
    position: relative;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
    margin-bottom: 1.5rem
}

.project-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 4px;
    height: 100%;
    background: var(--global-theme-color);
    transition: width 0.3s ease;
}

.project-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.15);
    border-color: var(--global-theme-color);
}

.project-card:hover::before {
    width: 6px;
}

.project-content {
    padding: 1.5rem;
    padding-left: 2rem;
}

.project-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 1rem;
}

.project-title {
    font-size: 1.4rem;
    font-weight: 600;
    color: var(--global-theme-color);
    margin: 0;
}

.project-links {
    display: flex;
    gap: 0.8rem;
}

.project-link {
    color: var(--global-text-color);
    transition: color 0.2s ease;
    display: flex;
    align-items: center;
}

.project-link:hover {
    color: var(--global-theme-color);
}

.project-link svg {
    width: 20px;
    height: 20px;
    fill: currentColor;
}

.project-link:hover svg {
    transform: scale(1.05);
}

.project-description {
    margin-bottom: 1.25rem;
}

.project-description ul {
    list-style-type: none;
    padding-left: 0;
}

.project-description li {
    position: relative;
    padding-left: 1.5rem;
    margin-bottom: 0.75rem;
    line-height: 1.6;
}

.project-description li::before {
    content: '•';
    position: absolute;
    left: 0;
    color: var(--global-theme-color);
    font-weight: bold;
}

.tech-stack {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    gap: 0.5rem;
    margin-top: 1rem;
}

.tech-label {
    font-weight: 600;
    margin-right: 0.5rem;
    font-size: 0.9rem;
    color: var(--global-text-color);
    align-self: center;
}

.tech-item {
    background-color: rgba(var(--global-theme-color-rgb), 0.1);
    color: var(--global-theme-color);
    padding: 0.3rem 0.8rem;
    border-radius: 20px;
    font-size: 0.85rem;
    font-weight: 500;
    line-height: 1.3;
    display: inline-flex;
    align-items: center;
}

@media (prefers-color-scheme: dark) {
    .project-card {
        box-shadow: 0 2px 8px rgba(255, 255, 255, 0.05);
    }

    .project-card:hover {
        box-shadow: 0 12px 24px rgba(255, 255, 255, 0.1);
    }

    .tech-item {
        background-color: rgba(var(--global-theme-color-rgb), 0.2);
    }
}

.projects-category {
    padding-bottom: 0;
}

.category-header {
    display: flex;
    align-items: center;
    cursor: pointer;
    padding: 0.5rem 0;
    margin-bottom: 1rem;
    border-bottom: 1px solid var(--global-divider-color);
}

.category-title {
    font-size: 1.6rem;
    font-weight: 600;
    color: var(--global-theme-color);
    margin: 0;
    position: relative;
    /* padding-left: 1.8rem; */
    padding-bottom: 1rem;
}

/* .category-title::before {
    content: '';
    position: absolute;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
    width: 1.2rem;
    height: 1.2rem;
    background-color: var(--global-theme-color);
    border-radius: 3px;
} */

.category-icon {
    margin-left: auto;
    transition: transform 0.3s ease;
}

.category-icon svg {
    width: 1.2rem;
    height: 1.2rem;
    fill: var(--global-text-color);
}

.category-expanded .category-icon {
    transform: rotate(90deg);
}

.category-projects {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
    overflow: hidden;
    transition: max-height 0.5s ease, opacity 0.3s ease;
}

/* Animation for collapsing/expanding */
.category-collapsed .category-projects {
    max-height: 0;
    opacity: 0;
}

.category-expanded .category-projects {
    max-height: 2000px; /* Adjust based on your content */
    opacity: 1;
}

</style>

<div class="projects-container">
    <div class="projects-category">
        <h2 class="category-title">Natural Language Processing & LLMs</h2>
        <div class="project-card">
            <div class="project-content">
                <div class="project-header">
                    <h3 class="project-title">Curriculum Compass: A RAG Chatbot for Personalized Course Guidance</h3>
                    <div class="project-links">
                        <a href="https://github.com/Kishore-Pratheesh-AI-Projects/course-registration-chatbot" class="project-link" aria-label="GitHub repository">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                            </svg>
                        </a>
                    </div>
                </div>

                <div class="project-description">
                    <ul>
                        <li>Engineered a <strong>Hybrid-RAG</strong> course registration assistant for Northeastern by fine-tuning <strong>Qwen2.5 0.5B</strong> with <strong>QLoRA</strong> and <strong>knowledge distillation</strong> on synthetic dataset from <strong>Llama3 7B</strong>, resulting in improved n-gram and <strong>LLM-as-judge</strong> metrics.</li>
                        <li>Automated <strong>ETL/model training</strong> pipelines  with <strong>Apache Airflow</strong> on <strong>GCP</strong> through <strong>Cloud Composer</strong> and <strong>BigQuery</strong>.
    Implemented <strong>CI/CD</strong> for ML workflows via <strong>GitHub Actions</strong> and <strong>Cloud Run</strong>, integrating <strong>Weights & Biases</strong> for model tracking.</li>
                    </ul>
                </div>
                
                <div class="tech-stack">
                    <span class="tech-label">Tech Stack:</span>
                    <span class="tech-item">Huggingface Transformers</span>
                    <span class="tech-item">Bitsandbytes</span>
                    <span class="tech-item">Apache Airflow</span>
                    <span class="tech-item">Weights and Biases</span>
                    <span class="tech-item">GCP</span>
                    <span class="tech-item">PyTorch</span>
                </div>
            </div>
        </div>

        <div class="project-card">
        <div class="project-content">
            <div class="project-header">
                <h3 class="project-title">TravelCompanion: Multi-Agent LLM System for Personalized Travel Planning</h3>
                <div class="project-links">
                    <a href="https://github.com/Kishore-Pratheesh-AI-Projects/TravelCompanion" class="project-link" aria-label="GitHub repository">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </a>
                </div>
            </div>
            
            <div class="project-description">
                <ul>
                    <li>Implemented a <strong>multi-agentic</strong> workflow using the <strong>ReAct framework</strong> (Chain of Thought) with <strong>OpenAI GPT-4 Turbo</strong>, <strong>LlamaIndex</strong> and <strong>custom tool calls</strong> for end-to-end travel planning and personalized recommendations</li>
                    <li>Automated <strong>CI/CD</strong> pipelines with <strong>GitHub Actions</strong>, containerized the application using <strong>Docker</strong> into <strong>AWS Elastic Container Registry</strong> (ECR) and deployed it on an <strong>EC2 instance</strong>.</li>
                </ul>
            </div>
            
            <div class="tech-stack">
                <span class="tech-label">Tech Stack:</span>
                <span class="tech-item">Huggingface Transformers</span>
                <span class="tech-item">LlamaIndex</span>
                <span class="tech-item">OpenAI</span>
                <span class="tech-item">Agentic AI</span>
                <span class="tech-item">Docker</span>
                <span class="tech-item">AWS</span>
                <span class="tech-item">PyTorch</span>
            </div>
        </div>
    </div>

    </div>

    <div class="projects-category">
        <h2 class="category-title">Computer Vision</h2>

    <!-- <div class="project-card">
        <div class="project-content">
            <div class="project-header">
                <h3 class="project-title">Pencil2Pixel: Gamma-Corrected GANs for Refined Forensic Sketch Generation</h3>
                <div class="project-links">
                    <a href="https://github.com/kishore-s-15/Pencil2Pixel" class="project-link" aria-label="GitHub repository">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </a>
                </div>
            </div>
            
            <div class="project-description">
                <ul>
                    <li>Designed a Conditional Pix2Pix GAN with grid search for forensic sketch enhancement resulting in a 31% increase in SSIM and a 35% boost in PSNR.</li>
                    <li>Evaluated the performance of Gamma-Corrected GANs using a ResNet-50 classifier on a custom celebrity dataset, resulting in a 10\% increase in classification accuracy with Gamma-inverted sketches.</li>
                </ul>
            </div>
            
            <div class="tech-stack">
                <span class="tech-label">Tech Stack:</span>
                <span class="tech-item">Huggingface Transformers</span>
                <span class="tech-item">Bitsandbytes</span>
                <span class="tech-item">Accelerate</span>
                <span class="tech-item">Weights and Biases</span>
                <span class="tech-item">Apache Airflow</span>
                <span class="tech-item">GCP</span>
            </div>
        </div>
    </div>
    -->

    <div class="project-card">
        <div class="project-content">
            <div class="project-header">
                <h3 class="project-title">Video Analytics for Cricket Shot Classification</h3>
                <div class="project-links">
                    <a href="https://github.com/kishore-s-15/Cricket-Shot-Prediction" class="project-link" aria-label="GitHub repository">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </a>
                </div>
            </div>
            
            <div class="project-description">
                <ul>
                    <li>Engineered <strong>EfficientNet-based CNNs with GRU</strong> integration integrating <strong>genetic algorithms</strong> for hyperparameter optimization to classify 30-frame video sequences of cricket shots into ten categories.</li>
                    <li>Achieved a <strong>peak accuracy and F1 score</strong> of 94% with the Efficient-B0 model and adapted cosine similarity algorithms to assess shot similarity enhancing analytical insights.</li>
                </ul>
            </div>
            
            <div class="tech-stack">
                <span class="tech-label">Tech Stack:</span>
                <span class="tech-item">Sequence Models</span>
                <span class="tech-item">PyTorch</span>
            </div>
        </div>
    </div>

    <div class="project-card">
        <div class="project-content">
            <div class="project-header">
                <h3 class="project-title">Diffusion Models for Image Generation</h3>
                <div class="project-links">
                    <a href="https://github.com/Kishore-Pratheesh-AI-Projects/Gray2RGB-Diffusion" class="project-link" aria-label="GitHub repository">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </a>
                </div>
            </div>
            
            <div class="project-description">
                <ul>
                    <li>Developed an <strong>image-to-image diffusion</strong> model for <strong>grayscale-to-RGB</strong> colorization using CIFAR-10, achieving Fréchet Inception Distance (FID) and Inception Score (IS) comparable to published research</li>
                    <li>Implemented and trained <strong>classifier-free and classifier-guided conditional diffusion</strong> models from scratch on MNIST, achieving <strong>92% and 94% classification accuracy</strong> on generated images.</li>
                </ul>
            </div>
            
            <div class="tech-stack">
                <span class="tech-label">Tech Stack:</span>
                <span class="tech-item">Huggingface Diffusers</span>
                <span class="tech-item">PyTorch</span>
            </div>
        </div>
    </div>
    </div>

    <div class="projects-category">
        <h2 class="category-title">Machine Learning / Analytics</h2>
        <div class="project-card">
            <div class="project-content">
                <div class="project-header">
                    <h3 class="project-title">ML Olympiad - Autism Prediction Challenge</h3>
                    <div class="project-links">
                        <a href="https://www.kaggle.com/competitions/autism-prediction/discussion/312152" class="project-link" aria-label="Live website">
                            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                                <path d="M11.99 2C6.47 2 2 6.48 2 12s4.47 10 9.99 10C17.52 22 22 17.52 22 12S17.52 2 11.99 2zm6.93 6h-2.95c-.32-1.25-.78-2.45-1.38-3.56 1.84.63 3.37 1.91 4.33 3.56zM12 4.04c.83 1.2 1.48 2.53 1.91 3.96h-3.82c.43-1.43 1.08-2.76 1.91-3.96zM4.26 14C4.1 13.36 4 12.69 4 12s.1-1.36.26-2h3.38c-.08.66-.14 1.32-.14 2 0 .68.06 1.34.14 2H4.26zm.82 2h2.95c.32 1.25.78 2.45 1.38 3.56-1.84-.63-3.37-1.9-4.33-3.56zm2.95-8H5.08c.96-1.66 2.49-2.93 4.33-3.56C8.81 5.55 8.35 6.75 8.03 8zM12 19.96c-.83-1.2-1.48-2.53-1.91-3.96h3.82c-.43 1.43-1.08 2.76-1.91 3.96zM14.34 14H9.66c-.09-.66-.16-1.32-.16-2 0-.68.07-1.35.16-2h4.68c.09.65.16 1.32.16 2 0 .68-.07 1.34-.16 2zm.25 5.56c.6-1.11 1.06-2.31 1.38-3.56h2.95c-.96 1.65-2.49 2.93-4.33 3.56zM16.36 14c.08-.66.14-1.32.14-2 0-.68-.06-1.34-.14-2h3.38c.16.64.26 1.31.26 2s-.1 1.36-.26 2h-3.38z"/>
                            </svg>
                        </a>
                    </div>
                </div>
                
                <div class="project-description">
                    <ul>
                        <li>Developed a high-performing two-level stacking <strong>ensemble</strong> classifier combining <strong>XGBoost, LightGBM, CatBoost, and Random Forest</strong> classifiers as base estimators with a final Logistic Regression model.</li>
                        <li>Resolved the unbalanced data problem using <strong>SMOTE</strong> and trained the model with stratified k-fold cross-validation, optimizing hyperparameters via a <strong>Bayesian tuning</strong> framework to achieve a test set <strong>AUC-ROC</strong> score of <strong>0.943</strong>.</li>
                    </ul>
                </div>
                
                <div class="tech-stack">
                    <span class="tech-label">Tech Stack:</span>
                    <span class="tech-item">Huggingface Transformers</span>
                    <span class="tech-item">Bitsandbytes</span>
                    <span class="tech-item">Accelerate</span>
                    <span class="tech-item">Weights and Biases</span>
                    <span class="tech-item">Apache Airflow</span>
                    <span class="tech-item">GCP</span>
                </div>
            </div>
        </div>
    </div>

    <div class="projects-category">
        <h2 class="category-title">Software Engineering</h2>
    <div class="project-card">
        <div class="project-content">
            <div class="project-header">
                <h3 class="project-title">Synapse - HR Analytics Dashboard</h3>
            </div>
            
            <div class="project-description">
                <ul>
                    <li>Created <strong>data visualization</strong> dashboard using <strong>Tableau</strong> to illustrate employee skill sets and proficiency levels, and utilized <strong>Django</strong> to transform the code into a <strong>REST API backend</strong> service and integrated with <strong>React Typescript</strong> frontend.</li>
                    <li>Devised an <strong>algorithm</strong> to assess <strong>employees' rankings</strong> within the dashboard, accounting for diverse skill sets and varying proficiency levels across the organization through a <strong>normalized scoring mechanism.</strong></li>
                </ul>
            </div>
            
            <div class="tech-stack">
                <span class="tech-label">Tech Stack:</span>
                <span class="tech-item">Data Visualization</span>
                <span class="tech-item">Tableau</span>
                <span class="tech-item">Django</span>
                <span class="tech-item">React Typescript</span>
                <span class="tech-item">Algorithms</span>
            </div>
        </div>
    </div>
    </div>
</div>

<script>
function toggleCategory(categoryElement) {
    categoryElement.classList.toggle('category-expanded');
    categoryElement.classList.toggle('category-collapsed');

    // If this is the initial state, we need to set max-height
    if (categoryElement.classList.contains('category-collapsed')) {
        const projects = categoryElement.querySelector('.category-projects');
        projects.style.maxHeight = '0';
    } else {
        const projects = categoryElement.querySelector('.category-projects');
        projects.style.maxHeight = projects.scrollHeight + 'px';
    }
}

// Initialize all categories as expanded by default
document.querySelectorAll('.projects-category').forEach(category => {
    category.classList.add('category-expanded');
    const projects = category.querySelector('.category-projects');
    projects.style.maxHeight = projects.scrollHeight + 'px';
});
</script>
