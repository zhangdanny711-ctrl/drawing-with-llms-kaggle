# Drawing with LLMs — Kaggle Solution

## Overview
This project is a solution to the Kaggle "Drawing with LLMs" competition, where the goal is to generate images from text prompts and evaluate how well they match semantic descriptions using automated scoring systems.

## Competition Description
In this competition, participants generate images based on textual descriptions and aim to align them with multiple-choice question-answer pairs. The evaluation measures how well generated images match the expected answers using automated similarity scoring methods (such as CLIP-style evaluation). The task combines generative modeling and evaluation pipeline design.

## Approach

### Image Generation
- Used Stable Diffusion XL (DreamShaper XL Turbo) to generate images from prompts
- Built a controlled generation pipeline for consistent outputs

### Prompt Engineering
- Designed structured prompts to guide generation:
  - prefix: "vector"
  - suffix: "flat color blocks, minimal details"
  - negative prompts to suppress unwanted features
- Improved alignment between generated images and evaluation metrics

### Scoring Pipeline
- Implemented a custom scoring function:
  - resized generated images
  - compared outputs against multiple-choice answers
  - used similarity-based evaluation

### End-to-End System
Text Prompt -> Diffusion Model -> Generated Image -> Scoring -> Selection

## Results
- Best Private Score: 0.68109
- Achieved through iterative prompt tuning and pipeline optimization

## Tech Stack
- Python
- PyTorch
- Diffusers (Stable Diffusion XL)
- Vision-language evaluation methods
- Pandas / NumPy

## Key Takeaways
- Prompt engineering plays a critical role in generative tasks
- Evaluation pipeline design is as important as model selection
- Diffusion models require structured prompting to produce usable outputs

## Notes
- This repository contains only code (no competition data)
