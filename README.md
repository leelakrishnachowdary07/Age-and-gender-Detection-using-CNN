# Age and Gender Detection using Convolutional Neural Networks (CNN)

This project aims to detect age and gender from images using a Convolutional Neural Network (CNN). Below is a detailed explanation of the project and its stages.

---

## **1. Overview of the Project**

- **Objective**: Predict age and gender from facial images using the UTKFace dataset.
- **Dataset**: The UTKFace dataset contains labeled images where filenames include age, gender, and other attributes.
- **Approach**: A CNN-based model processes grayscale images, extracts features, and predicts:
  - **Gender**: A binary classification task (Male/Female).
  - **Age**: A regression task (continuous value).

---

## **2. Loading the Dataset**

- **Why?** The dataset provides the foundational data for training the model. Each image contains information about age and gender in its filename.
- **What we did**: Extracted image paths and parsed filenames to derive age and gender labels. Organized this data into a structured format (dataframe) for further processing.

---

## **3. Exploratory Data Analysis (EDA)**

- **Why?** To understand the dataset's structure, verify labels, and visualize data distribution.
- **What we did**:
  - Displayed a sample grid of images to confirm the association between images and labels.
  - Analyzed label distributions to check for imbalances or anomalies in the dataset.

---

## **4. Feature Extraction**

- **Why?** Neural networks require consistent input sizes and normalized values for effective learning.
- **What we did**:
  - Converted images to grayscale to simplify processing.
  - Resized images to 128x128 pixels for uniformity.
  - Normalized pixel values to range between 0 and 1 for better numerical stability during training.

---

## **5. Model Architecture**

- **Why?** CNNs are effective for image-based tasks due to their ability to learn spatial hierarchies of features.
- **What we designed**:
  - **Input Layer**: Accepts preprocessed grayscale images.
  - **Convolutional Layers**: Extract spatial features from images using filters of increasing depth.
  - **Pooling Layers**: Downsample feature maps to reduce spatial dimensions and computational load.
  - **Fully Connected Layers**: Combine extracted features to make predictions for age and gender.
  - **Outputs**:
    - **Gender**: A binary classification output using sigmoid activation.
    - **Age**: A regression output using ReLU activation.

---

## **6. Model Training**

- **Why?** To learn patterns and relationships in the dataset for predicting age and gender.
- **What we used**:
  - **Loss Functions**:
    - Gender: Binary Cross-Entropy for classification.
    - Age: Mean Absolute Error (MAE) for regression.
  - **Optimizer**: Adam, for adaptive learning rates.
  - **Validation Split**: 20% of the data was used for validation to monitor the model's performance on unseen data.

---

## **7. Results and Visualization**

- **Why?** To evaluate the model’s performance and ensure it generalizes well to unseen data.
- **What we analyzed**:
  - Plotted training and validation accuracy for gender prediction.
  - Visualized loss curves to identify overfitting or underfitting.
  - Reported final training and validation accuracy.

---

## **8. Predictions on Test Data**

- **Why?** To assess the model's effectiveness in real-world scenarios.
- **What we did**:
  - Used test images to generate predictions for age and gender.
  - Compared predictions with true labels to evaluate accuracy.
  - Visualized sample predictions alongside the original images.

---

## **9. Key Takeaways**

- **Model Performance**: The CNN-based model effectively predicts age and gender with acceptable accuracy.
- **Challenges**:
  - Imbalanced dataset leading to potential biases.
  - Noise in age labels affecting regression accuracy.
- **Future Improvements**:
  - Use Transfer Learning for enhanced feature extraction.
  - Implement data augmentation to mitigate overfitting and improve generalization.

---

Link:
https://colab.research.google.com/drive/19JWGJlGD9M6UpFFuIf0XemvtekcZmgFZ?usp=sharing
