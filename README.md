# PROJECT-Alzheimer's Disease Stage Detection
This project uses a deep learning model (fine-tuned VGG16) to classify brain MRI images into different stages of Alzheimer's disease. The model is deployed via Gradio on Hugging Face Spaces, making it fully accessible through a clean web interface.

## Overview:

This project uses a deep learning model (fine-tuned VGG16) to classify **brain MRI images** into different stages of Alzheimer's disease. The model is deployed via **Gradio** on **Hugging Face Spaces**, making it fully accessible through a clean web interface.

## Live Demo
 **[Gradio](https://huggingface.co/spaces/anurag4real/Alzheimer_Disease_Stage_Detection)**


## 💡 Problem Statement

Alzheimer’s disease is a progressive brain disorder. Early detection and stage identification are crucial for timely treatment. This model aims to assist in classifying MRI scans into one of the following four categories:

-  ModerateDemented  
-  MildDemented  
-  VeryMildDemented  
-  NonDemented


## Model Details:

- **Base Model**: VGG16
- **Fine-tuning**: Top layers retrained for 4-class classification
- **Top Layers**:
  - `GlobalAveragePooling2D`
  - `Dense(256, ReLU)` + `Dropout` + `BatchNorm`
  - `Dense(4, Softmax)`
- **Loss Function**: `sparse_categorical_crossentropy`
- **Optimizer**: Adam (learning rate = 0.0001)
- **Input Size**: 224 × 224 × 3
- **Final Accuracy**: 96% on validation set


## Dataset

- Source: Kaggle (uploaded here)
- 4 classes with balanced sample counts
- Split into training and validation sets
- Augmentation applied via ImageDataGenerator


## Deployment

- Platform: Hugging Face Spaces

- Framework: Gradio

- Model size: ~113 MB

- Startup time: ~3 sec

