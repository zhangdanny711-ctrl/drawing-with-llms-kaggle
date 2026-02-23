# Drawing with LLMs — Kaggle Solution

## Overview
Built an end-to-end generative AI pipeline for the Kaggle "Drawing with LLMs" competition, transforming text prompts into images using diffusion models and optimizing outputs with a custom scoring system.

## Problem
The task is to generate images that accurately match textual descriptions and align with multiple-choice answers using automated evaluation metrics.

## Approach

### Image Generation
- Used Stable Diffusion XL (DreamShaper XL Turbo) to generate images from text prompts
- Designed a controlled generation pipeline for consistency

### Prompt Engineering
- Applied structured prompting:
  - prefix: "vector"
  - suffix: "flat color blocks, minimal details"
  - negative prompts to suppress noise
- Improved alignment with evaluation metrics

### Scoring Pipeline
- Implemented a custom evaluation function:
  - resized generated images
  - compared outputs against candidate answers
  - used similarity-based scoring (CLIP-style)

### Pipeline
Text → Diffusion Model → Image → Scoring → Selection

## Results
- Best Private Score: 0.68109

## Tech Stack
- Python
- PyTorch
- Diffusers (Stable Diffusion XL)
- Vision-language evaluation methods
- Pandas / NumPy

## Key Takeaways
- Prompt engineering significantly impacts generative performance
- Evaluation design is critical in ML systems
- Diffusion models require structured constraints for reliable outputs

## Notes
- This repository contains code only (no competition data)
