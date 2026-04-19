# Sleep Stage Classification Project

## Project Overview
This project focuses on developing an automated system for classifying sleep stages using deep learning. By analyzing multi-channel physiological signals—including Electroencephalogram (EEG), Electrooculogram (EOG), and Electromyogram (EMG)—the model aims to accurately identify different sleep phases (Wake, N1, N2, N3, and REM). This automation assists in diagnosing sleep disorders and enhances the efficiency of sleep studies.

## Key Project Stages
The project follows a structured pipeline to ensure robust data processing and model performance:

1. **Data Exploration**: Initial analysis and visualization of raw EDF signals and XML annotations to understand signal characteristics across different sleep stages.
2. **Preprocessing**: 
   - Downsampling signals to 100Hz for computational efficiency.
   - Segmenting continuous recordings into standard 30-second epochs.
   - Normalizing and splitting data into Training, Validation, and Testing sets.
3. **Distribution Analysis**: Analyzing class distribution to address the inherent imbalance in sleep stage data.
4. **Model Architecture**: Implementation of a hybrid Deep Learning model:
   - **CNN Layers**: For spatial feature extraction from raw signals.
   - **LSTM Layers**: For capturing temporal dependencies and sequential patterns.
5. **Evaluation**: Assessing the model using Accuracy, Precision, Recall, F1-Score, and Confusion Matrices.

## Requirements
To run this project, ensure you have Python installed along with the following libraries:
```bash
pip install -r requirements.txt
