# Breast Cancer Classification Using Neural Network

This project uses a neural network to classify breast cancer cases as either malignant or benign based on a set of features in the dataset. The model is trained on data from `sklearn.datasets.load_breast_cancer`, using 30 distinct features for each sample, such as mean radius, texture, area, smoothness, compactness, and other characteristics relevant to diagnosis.

## Project Overview

The project demonstrates the application of a neural network to solve a binary classification problem, where the goal is to predict if a tumor is malignant or benign. The project utilizes the following key components and techniques:

- **Data Loading and Preprocessing**: The dataset is loaded from `sklearn` and preprocessed using a `StandardScaler` to standardize feature values for optimal neural network performance.
- **Neural Network Architecture**:
  - **Input Layer**: Takes in 30 features corresponding to different attributes of each tumor.
  - **Hidden Layer**: A single hidden layer with 20 neurons and ReLU activation function.
  - **Output Layer**: Contains 2 neurons (one for each class) with a sigmoid activation function for binary classification.
- **Training and Validation**: The model is trained for 10 epochs with a split of training and validation data to track model performance.
- **Performance Evaluation**: Model performance is evaluated using accuracy on test data, along with plotting training and validation accuracy and loss over epochs.
- **Prediction and Inference**: A sample input is processed and fed into the model to predict whether a tumor is malignant or benign.

## Dataset Details

The dataset includes 569 samples and 30 features for each sample. The target variable is a binary label, with:
- `1` indicating a benign tumor
- `0` indicating a malignant tumor

### Features in Dataset

- `mean radius`
- `mean texture`
- `mean perimeter`
- `mean area`
- `mean smoothness`
- `mean compactness`
- `mean concavity`
- `mean concave points`
- `mean symmetry`
- `mean fractal dimension`
- `radius error`
- `texture error`
- `perimeter error`
- `area error`
- `smoothness error`
- `compactness error`
- `concavity error`
- `concave points error`
- `symmetry error`
- `fractal dimension error`
- `worst radius`
- `worst texture`
- `worst perimeter`
- `worst area`
- `worst smoothness`
- `worst compactness`
- `worst concavity`
- `worst concave points`
- `worst symmetry`
- `worst fractal dimension`

## Code Summary

1. **Data Preparation**:
   - Loading data and adding target labels to a DataFrame.
   - Splitting data into training and test sets with an 80-20 ratio.
   - Standardizing the feature values to improve model performance.

2. **Model Architecture and Training**:
   - Constructing a neural network with `keras.Sequential`.
   - Compiling the model using `Adam` optimizer and sparse categorical cross-entropy loss.
   - Training with `fit` function, tracking accuracy and loss on both training and validation sets.

3. **Evaluation and Prediction**:
   - Evaluating model performance on the test data.
   - Plotting accuracy and loss metrics for both training and validation sets.
   - Predicting the classification for a sample input and determining if the tumor is malignant or benign.

## Example Output

For a given input sample, the model predicts:
- **Benign** if the prediction label is `1`
- **Malignant** if the prediction label is `0`

---

This project demonstrates how to apply a neural network to medical data for binary classification, providing a foundation for more complex models and medical diagnostic applications.
