# Drawing with LLMs — Kaggle Solution

## Overview
This project is a solution to the Kaggle **"Drawing with LLMs"** competition, where the goal is to generate images (SVG/bitmap) from text prompts and evaluate their semantic alignment using vision-language models.

## Problem
Participants must generate images that best match a given textual description. The generated outputs are evaluated based on how well they align with multiple-choice question-answer pairs using automated scoring systems.

---

## Approach

### 1. Data Processing
- Loaded competition data (`train.csv`, question-answer pairs)
- Structured QA pairs into grouped format for evaluation

### 2. Image Generation
- Used **Stable Diffusion XL (DreamShaper XL Turbo)** via `diffusers`
- Generated bitmap images from text prompts

### 3. Prompt Engineering
- Designed structured prompts:
  - Prefix: `"vector"`
  - Suffix: `"flat color blocks, minimal details"`
  - Negative prompts to suppress unwanted features
- Improved generation quality and consistency

### 4. Scoring Mechanism
- Implemented custom scoring function:
  - Resized generated images
  - Compared outputs against multiple-choice answers
  - Used similarity-based evaluation (CLIP-style scoring)

### 5. End-to-End Pipeline
Text Prompt → Diffusion Model → Generated Image → Scoring → Selection

---

## Results
- **Best Private Score:** 0.68109
- Iterative improvement through prompt tuning and model selection

---

## Tech Stack
- Python
- PyTorch
- Diffusers (Stable Diffusion XL)
- CLIP-style evaluation
- Pandas / NumPy

---

## Key Insights
- Prompt engineering significantly impacts generation quality
- Diffusion models require style constraints to align with evaluation metrics
- Scoring pipeline design is as important as generation

---

## Notes
- No competition data is included in this repository
