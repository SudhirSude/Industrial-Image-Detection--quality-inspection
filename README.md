# Industrial Casting Defect Detection with CNN


## Project Overview

Automated quality inspection system for detecting defects in casting products using deep learning. Achieves 98.7% accuracy in classifying casting images as defective or non-defective.

## Dataset

- **Images**: 7,348 total (6,633 train, 715 test)
- **Classes**:
  - Defective (453 test samples)
  - Non-defective (262 test samples)
- **Defect Types**: Blow holes, pinholes, burrs, shrinkage, etc.

## Model Architecture

3-layer CNN with:
- Conv2D layers (16, 32, 64 filters)
- MaxPooling after each conv layer
- 224-unit Dense layer with Dropout
- Binary classification output

**Total Parameters**: 4.7 million

## Results

### Performance Metrics
| Class     | Precision | Recall | F1-Score |
|-----------|-----------|--------|----------|
| Defective | 1.000     | 0.980  | 0.990    |
| OK        | 0.967     | 1.000  | 0.983    |

**Overall Accuracy**: 98.7%

## Key Features

- Comprehensive data augmentation
- Early stopping and model checkpointing
- Detailed error analysis
- Visual prediction examples

## Training

- **Epochs**: 20 (early stopped at 3)
- **Batch Size**: 32
- **Optimizer**: Adam
- **Final Val Accuracy**: 96.1%
