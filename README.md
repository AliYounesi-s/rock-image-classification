## Rock Image Classification (CNN from Scratch)

This project implements a convolutional neural network (CNN) trained **from scratch** to classify rock images into multiple geological categories using PyTorch.  
The focus of the project is on building a complete, transparent ML pipeline and performing meaningful error analysis rather than achieving state-of-the-art accuracy.

---

## Project Overview

- Multi-class image classification of rock types
- Custom CNN architecture implemented from scratch (no pretrained backbones)
- Dataset prepared locally and used in Google Colab for training
- Full training, evaluation, and analysis workflow

---

## Workflow

1. **Data preparation (local)**
   - Raw images cleaned and converted to JPEG
   - Dataset split into `train/` and `test/` directories compatible with `ImageFolder`
   - Prepared dataset uploaded to Google Colab

2. **Data loading**
   - `torchvision.datasets.ImageFolder`
   - Separate transforms for training and testing
   - Normalization using ImageNet statistics

3. **Model**
   - CNN built from scratch using PyTorch
   - Two convolutional blocks + fully connected classifier
   - Input size fixed at `64×64`

4. **Training**
   - CrossEntropyLoss
   - Adam optimizer
   - Custom training and evaluation loops
   - Best model selected based on test performance

5. **Evaluation**
   - Accuracy tracking
   - Confusion matrix
   - Qualitative inspection of correct vs incorrect predictions

---

## Results

- Best test accuracy achieved after **epoch 2**
- Strong performance on visually distinctive classes (e.g. Coal, Sandstone)
- Significant confusion between visually similar rock types (e.g. Limestone, Marble, Granite)
- Overfitting observed with further training, highlighting generalization limits

---

## Error Analysis

- Confusion matrix reveals structured (non-random) misclassifications
- Errors align with geological and visual similarity between classes
- Qualitative visualization used to inspect misclassified samples

---


