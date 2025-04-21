# Alphabet Image Classification

This project classifies handwritten alphabet images into their corresponding labels using machine learning models. The dataset contains images of letters that are processed, resized, and used for training different models. The objective is to compare the performance of multiple classifiers and determine the best model for this task.

## Table of Contents

1. [Setup](#setup)
2. [Data Preprocessing](#data-preprocessing)
3. [Feature Extraction](#feature-extraction)
4. [Model Training & Evaluation](#model-training--evaluation)
5. [Results](#results)
6. [Conclusion](#conclusion)

---

## Setup

In this project, several Python libraries are used, including `PIL`, `numpy`, `pandas`, and `sklearn`. Additionally, Google Drive is mounted to save and load datasets.

---

## Data Preprocessing

The dataset is located in a folder named `/content/sample_data/New folder`. The images are organized in subfolders representing different letters. These images are loaded into the program, and their labels are extracted from the filenames.

---

## Feature Extraction

### Image Resizing

The images are resized to 15x15 pixels using the `thumbnail()` method. This reduces the size of the input features for easier processing.

### Flattening the Images

Each image is flattened into a one-dimensional array, which is then used as input for machine learning models. The resulting data is stored in a pandas DataFrame with a column for labels.

### Saving the DataFrame

The DataFrame containing the image data and labels is saved as a CSV file for further use in training and testing machine learning models.

---

## Model Training & Evaluation

The dataset is split into training and test sets. Several machine learning classifiers are then trained using the training set, and their performance is evaluated using the test set.

---

## Results

The classifiers are evaluated based on accuracy, with the following results:

| Algorithm                 | Classification  | Accuracy  |
|---------------------------|-----------------|-----------|
| LogisticRegression         | Logit           | 0.356288  |
| DT Classifier              | Decision-Tree   | 0.927873  |
| Random Forest Classifier   | Ensemble        | 0.977017  |
| AdaBoost-Boosting Classifier | Boosting        | 0.537530  |
| Bagging Classifier         | Bagging         | 0.954249  |

---

## Conclusion

- **Random Forest Classifier** achieved the highest accuracy (97%), outperforming all other models.
- **Bagging Classifier** followed closely with an accuracy of 95%.
- **Decision Tree Classifier** showed a solid performance with an accuracy of 92%.
- **AdaBoost Classifier** and **Logistic Regression** performed significantly worse.

These results suggest that **Random Forest** is the most effective model for this particular classification task. Further evaluation and validation are needed to confirm this conclusion.
