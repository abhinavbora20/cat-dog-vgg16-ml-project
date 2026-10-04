# Cat vs Dog Classification Using VGG16

## Project Overview

This project implements a binary image classification system to distinguish between **Cats** and **Dogs** using **VGG16 transfer learning and fine-tuning**.

The project uses a pretrained VGG16 convolutional neural network and adapts it for Cat vs Dog classification. After initial transfer learning, the final four VGG16 layers were fine-tuned to improve performance.

## Dataset

The dataset contains **24,998 usable images** belonging to two classes:

- Cat
- Dog

### Dataset Split

| Dataset | Number of Images |
|---|---:|
| Training | 19,998 |
| Validation | 2,500 |
| Test | 2,500 |
| **Total** | **24,998** |

The dataset itself is not included in this repository because of its size.

## Methodology

The project follows these main steps:

1. Dataset preparation and validation
2. Image preprocessing
3. Data augmentation
4. VGG16 transfer learning
5. Baseline model training
6. Baseline evaluation
7. Fine-tuning of the final four VGG16 layers
8. Fine-tuned model evaluation
9. Confusion matrix and classification metrics
10. Confidence-based prediction
11. Final model verification

### Input

Images are resized to:

```text
224 × 224 × 3
```

### Model

**Architecture:** VGG16

**Approach:**

- Transfer Learning
- Fine-Tuning

## Results

### Baseline Model

| Metric | Result |
|---|---:|
| Test Accuracy | 97.52% |
| Test Loss | 0.0656 |

### Fine-Tuned Model

| Metric | Result |
|---|---:|
| Test Accuracy | **98.68%** |
| Test Loss | **0.0364** |
| Precision | **98.95%** |
| Recall | **98.40%** |

Fine-tuning improved the test accuracy from **97.52% to 98.68%**.

## Confusion Matrix

The final fine-tuned model produced the following results on the 2,500-image test set:

| | Predicted Cat | Predicted Dog |
|---|---:|---:|
| **Actual Cat** | 1237 | 13 |
| **Actual Dog** | 20 | 1230 |

## Custom Feature

The project includes a **Confidence-Based Prediction Feedback** feature.

For an input image, the system displays:

- Predicted class
- Confidence percentage
- Confidence level

The confidence level is categorized as:

- High
- Moderate
- Low

This provides additional information about how confidently the model makes each prediction.

## Additional Testing

An additional random sample of 10 test images was evaluated:

```text
Images tested: 10
Correct predictions: 10
Sample accuracy: 100%
```

This is an additional sample test and is separate from the official test-set accuracy of **98.68%**.

## Project Structure

```text
cat-dog-vgg16-ml-project/
│
├── notebooks/
│   └── Cat_Dog_VGG16.ipynb
│
├── model/
│   └── final_vgg16_finetuned.keras
│
├── results/
│   ├── fine_tuned_accuracy.png
│   ├── fine_tuned_loss.png
│   ├── fine_tuned_confusion_matrix.png
│   └── final_results_summary.txt
│
├── app/
│   └── [application files will be added]
│
├── error_analysis/
│   └── [error analysis files will be added]
│
├── .gitignore
└── README.md
```

## How to Run

The main machine-learning workflow is provided in:

```text
notebooks/Cat_Dog_VGG16.ipynb
```

The notebook contains the dataset preparation, VGG16 transfer-learning workflow, fine-tuning, evaluation, final model saving, and prediction functionality.

The application setup and execution instructions will be added after integration of the final application.

## Final Model

The final model is the fine-tuned VGG16 model:

```text
final_vgg16_finetuned.keras
```

The final model achieved:

**98.68% test accuracy**

on the 2,500-image test set.

## Team

This is a two-person ML project.

### Team Member 1
Abhinav Bora

### Team Member 2
[Teammate Name]

## Contributions

### Abhinav Bora

- Dataset preparation and validation
- Data preprocessing
- Data augmentation
- VGG16 transfer learning
- Baseline model training
- VGG16 fine-tuning
- Model evaluation
- Confusion matrix and classification metrics
- Confidence-based prediction feature
- Final model verification

### Team Member 2

Application development and additional project contributions will be documented after integration.

## Technologies Used

- Python
- TensorFlow / Keras
- VGG16
- Google Colab
- NumPy
- Matplotlib
- scikit-learn
- Git / GitHub