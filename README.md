# Skin Cancer Classification Project

## Table of Contents
* [General Information](#general-information)
* [Technologies Used](#technologies-used)
* [Model Training and Findings](#model-training-and-findings)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)
* [Contact](#contact)

## General Information
This project focuses on skin cancer classification using deep learning. The goal is to develop a CNN-based model to classify different types of skin lesions using the **ISIC The International Skin Imaging Collaboration** dataset.

### Dataset Details
- The dataset contains images of different skin conditions.
- It is divided into training and testing sets.
- The dataset is preprocessed and split into training (80%) and validation (20%) sets.

## Technologies Used
- Python
- TensorFlow/Keras
- Matplotlib for visualization
- Google Colab for training

## Model Training and Findings
### Phase 1: Training Without Augmentation
- Initial training was conducted on raw data.
- Observed **overfitting**:
  - Training accuracy improved significantly (25.09% → 86.3%)
  - Training loss reduced (2.0168 → 0.3734)
  - Validation accuracy peaked around 52% and then declined
  - Validation loss increased (1.6675 → 2.2936)

**Conclusion**: The model performed well on training data but failed to generalize, indicating overfitting.

### Phase 2: Applying Data Augmentation
- To improve generalization, the following augmentations were applied:
  - Random flipping (horizontal & vertical)
  - Random rotation (up to 20 degrees)
  - Random zoom (slight zoom-in)
  - Brightness adjustments (small variations)
  - Random translation

- Results after augmentation:
  - Improved generalization
  - Overfitting reduced

### Phase 3: Handling Class Imbalance
- **Augmentor** library was used to balance the dataset
- Improved class distribution helped stabilize model performance

## Conclusions
- Data augmentation helped reduce overfitting.
- Class balancing improved performance on underrepresented classes.
- Model generalization improved significantly.

## Acknowledgements
- Inspired by ISIC dataset research.
- Used TensorFlow documentation for model training guidance.
- Based on deep learning tutorials for medical image classification.

## Contact
Created by **[jeet-Suthar](https://github.com/jeet-Suthar)** - Feel free to reach out for collaborations or queries!

