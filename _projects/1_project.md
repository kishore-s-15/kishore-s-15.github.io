---
layout: page
title: Curriculum Compass
description: A RAG Chatbot for Personalized Course Guidance
img: assets/img/projects/course_curriculum.png
importance: 1
category: academic
related_publications: false
---

### Overview

Curriculum Compass is a Retrieval-Augmented Generation (RAG) system designed to streamline course selection at Northeastern University. The system integrates real-time course offerings from the NU Banner API with historical course reviews from NuTrace to provide comprehensive course selection guidance. By implementing both a hybrid RAG architecture and an agent-based framework, the system processes student queries to deliver accurate, context-aware responses for course selection decisions.

### Architecture

Curriculum Compass derives its core functionality from a dual-component architecture designed to process and deliver course information through multiple specialized subsystems. Its primary implementation uses a hybrid Retrieval-Augmented Generation (RAG) pipeline that combines TF-IDF and dense embedding techniques for information retrieval. This design facilitates the efficient handling of both structured course data and unstructured student reviews, thereby ensuring comprehensive coverage of all available course details.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/curriculum_project_arch.png' | relative_url }}" alt="Complete system architecture of Curriculum Compass" title="Complete system architecture of Curriculum Compass"/>
    </div>
</div>
<div class="caption">
    Complete system architecture showing the data pipeline, query processing, and hybrid RAG components
</div>

### Data Integration and Retrieval

The system's data integration module processes two main sources of information: current course listings from the NU Banner API and historical student feedback extracted from NuTrace PDFs. Course data includes schedules, prerequisites, and course descriptions, whereas review data provides insights such as student experiences, course difficulty levels, and teaching style feedback. Course information retrieval employs a hybrid approach merging TF-IDF-based search and dense embeddings, while reviews leverage dense embeddings stored in ChromaDB. Upon receiving a query, the system retrieves content in parallel from both sources and then applies cross-encoder-based reranking to the combined results, identifying the most relevant information. This refined context is subsequently passed to a Large Language Model (LLM), which generates coherent and contextually appropriate responses that integrate both course details and student perspectives.

### Agent-Based Framework

Building on the foundational RAG pipeline, the system also incorporates an alternative agent-based framework that provides more granular control over query processing and response generation. In this framework, specialized agents operate in coordination under an orchestration system. The ValidationAgent initially verifies whether the query is pertinent to NEU academics. Next, the IntentAgent analyzes the query's purpose and maps it to the available data structures. Subsequently, the QueryEnhancementAgent refines the query for database retrieval by generating targeted search parameters for both the course and review databases.

### Iterative Retrieval and Context Analysis

The DynamicRetrievalAgent manages the retrieval strategy, determining optimal retrieval parameters (k-values) for each database and executing the searches. Once results are obtained, the ContextAnalysisAgent assesses the completeness and relevance of the information. If the retrieved data proves insufficient, the ContextAnalysisAgent provides detailed feedback on missing elements and suggests adjustments to the retrieval process. This feedback triggers an iterative cycle wherein the DynamicRetrievalAgent modifies its strategy and performs additional retrievals. The loop continues for a specified number of iterations—up to four—or until the ContextAnalysisAgent concludes that sufficient information has been collected or that the query cannot be answered using the available data. If data remains incomplete or unavailable after these steps, the system may suggest alternative questions or approaches to help users obtain relevant information.

### Response Generation

Ultimately, the ResponseAgent compiles the final output, incorporating all retrieved information as well as any noted limitations. This multi-agent approach ensures thorough information gathering and validation prior to producing a response, with built-in procedures to handle scenarios where complete information is not attainable.

### Technical Implementation

From a technical perspective, the system employs the Qwen-0.5B model as its foundational component, enhanced through QLoRA fine-tuning for improved performance. It utilizes ChromaDB for vector storage and implements a cross-encoder architecture for response ranking.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/projects/curriculum_compass_pipeline.png' | relative_url }}" alt="Curriculum Compass Training Pipeline" title="Curriculum Compass Training Pipeline"/>
    </div>
</div>
<div class="caption">
    Training and evaluation pipeline showing synthetic data generation, model fine-tuning, and comprehensive evaluation process
</div>

### Query Processing Workflow

A multi-stage validation pipeline underpins the query processing workflow, ensuring both relevance and accuracy. Each query undergoes an initial assessment for academic suitability, followed by intent analysis and subsequent query enhancement. The retrieval process dynamically adapts based on specific query requirements, implementing feedback loops in instances where initial results prove insufficient. This design allows the system to handle diverse query types, ranging from highly specific course-related inquiries to broader academic planning questions.