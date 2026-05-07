# Sleep Stage Classification using Deep Learning (EOG-R)

## Overview

This project presents a deep learning-based system for automatic sleep stage classification using physiological sleep signals.

The model analyzes the **EOG-R signal** from the MESA Sleep Dataset and classifies sleep into five stages:

- Wake
- N1
- N2
- N3
- REM

The goal is to automate traditional manual sleep scoring using deep learning.

---

## Problem Statement

Traditional sleep stage scoring is:

- Time-consuming
- Expensive
- Requires expert analysis
- Prone to human error

This project builds an automated deep learning model for sleep stage classification.

---

## Dataset

### MESA Sleep Dataset

A public medical dataset containing overnight sleep recordings.

Includes:

- EDF signal files
- XML annotation files
- Expert-labeled sleep stages

Signals available:

- EEG
- EOG
- EMG
- ECG
- Respiratory signals

This project uses:

**EOG-R only**

---

## Sleep Classes

| Class | Description |
|------|-------------|
| Wake | Awake |
| N1 | Light Sleep |
| N2 | Intermediate Sleep |
| N3 | Deep Sleep |
| REM | Rapid Eye Movement |

---

## Workflow

### 1. Data Visualization
Visual inspection of raw signals and sleep stages.

### 2. Data Split

- Training: 60%
- Validation: 20%
- Testing: 20%

Subject-level split to avoid data leakage.

### 3. Preprocessing

Applied preprocessing steps:

- Channel selection (EOG-R)
- Bandpass filtering (0.5–20 Hz)
- Resampling to 100 Hz
- Z-score normalization
- Signal clipping
- 30-second epoch segmentation

Processed data stored as `.npz`.

---

## Model Architecture

Custom hybrid architecture:

- CNN
- Residual Blocks
- Squeeze-and-Excitation Attention
- BiLSTM
- Multi-Head Self Attention
- Dense Classifier

---


## Key Contribution

This work shows that effective sleep stage classification can be achieved using only the **EOG-R channel**, reducing dependence on full PSG systems.

---



## Author

**Eman Sabry**  
**Sara Mohamed**  
Biomedical Engineering Student  
Helwan University
## Requirements
To run this project, ensure you have Python installed along with the following libraries:
```bash
pip install -r requirements.txt
