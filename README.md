# Transfer Learning for Skin Lesion Classification

## Problem Statement
This project focuses on leveraging transfer learning with pre-trained models (VGG16, ResNet50, and InceptionV3) to classify skin lesions using the **ISIC Skin Lesion Dataset**. The dataset consists of images of skin lesions and metadata including lesion type, patient demographics, and diagnostic information.

Our mission is to explore how transfer learning can enhance healthcare infrastructure, specifically in regions with limited resources like Chad, by improving diagnostic accuracy and efficiency in dermatology through AI.

## Dataset
The **ISIC Skin Lesion Dataset** contains thousands of labeled images representing various skin conditions, including melanomas and benign lesions. The dataset is split into 80% training and 20% validation subsets, ensuring a balanced representation of the different classes in both sets.

## Evaluation Metrics
To assess the performance of the fine-tuned models, we used the following metrics:
- **Accuracy**: Measures the proportion of correctly predicted instances.
- **Loss**: The categorical cross-entropy loss used for optimization.
- **Precision**: The ability of the model to return only relevant instances.
- **Recall**: The ability of the model to identify all relevant instances.
- **F1 Score**: The harmonic mean of precision and recall, providing a single performance metric.

## Experiment Findings
Transfer learning proved to be a powerful tool for this healthcare application. Each of the pre-trained models demonstrated strengths in different areas:
- **VGG16**: Balanced performance across all metrics.
- **ResNet50**: Excelled in accuracy and F1 score, making it suitable for complex image classification tasks.
- **InceptionV3**: Showed potential but underperformed compared to the other models due to its deeper architecture requiring more data to reach peak performance.

### Strengths of Transfer Learning
- **Quick adaptation** to new datasets with minimal fine-tuning.
- **Pre-trained features** help overcome limited data availability in specialized domains like healthcare.

### Limitations of Transfer Learning
- **Model complexity**: Larger models like InceptionV3 may struggle with smaller datasets due to overfitting.
- **Domain-specific nuances**: Pre-trained models may not fully capture the unique characteristics of medical imagery.

## Model Evaluation

| Model       | Accuracy | Loss  | Precision | Recall | F1 Score |
|-------------|----------|-------|-----------|--------|----------|
| **VGG16**   | 0.75     | 0.93  | 0.74      | 0.75   | 0.74     |
| **ResNet50**| 0.80     | 0.85  | 0.79      | 0.80   | 0.79     |
| **InceptionV3** | 0.72  | 1.05  | 0.71      | 0.72   | 0.71     |

This table summarizes the performance of the models based on the evaluation metrics. **ResNet50** emerged as the best-performing model with the highest accuracy and F1 score. 

## Conclusion
This experiment demonstrates the potential of transfer learning in improving diagnostic accuracy in resource-constrained healthcare settings. ResNet50, with its deep architecture and strong performance metrics, is well-suited for deployment in real-world applications. However, more experimentation with larger datasets could further improve the performance of models like InceptionV3.
