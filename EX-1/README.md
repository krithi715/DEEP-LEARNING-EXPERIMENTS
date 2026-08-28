# Artificial Neural Network (ANN) for Regression

## AIM

To understand the implementation of an **Artificial Neural Network (ANN)** using TensorFlow and evaluate its performance on a regression problem using the **California Housing Dataset**.

---

## LEARNING OBJECTIVES

After completing this experiment, students will be able to:

1. Understand the architecture of an Artificial Neural Network.
2. Build an ANN model for regression problems.
3. Train and evaluate neural network models.
4. Make predictions using a trained ANN model.
5. Compare different regression evaluation metrics.

---

## SOFTWARE REQUIREMENTS

* Python 3.x
* Google Colab / Jupyter Notebook
* TensorFlow 2.x
* NumPy
* Pandas
* Matplotlib
* Scikit-learn

---

## DATASET

### California Housing Dataset

**Source:** Scikit-learn

The California Housing Dataset is a regression dataset used to predict the **median house value** based on various housing and demographic features.

| Property           | Details            |
| ------------------ | ------------------ |
| Number of Samples  | 20,640             |
| Number of Features | 8                  |
| Problem Type       | Regression         |
| Target             | Median House Value |
| Dataset Source     | Scikit-learn       |

### Features

| Feature      | Description                |
| ------------ | -------------------------- |
| `MedInc`     | Median Income              |
| `HouseAge`   | House Age                  |
| `AveRooms`   | Average Number of Rooms    |
| `AveBedrms`  | Average Number of Bedrooms |
| `Population` | Population                 |
| `AveOccup`   | Average Occupancy          |
| `Latitude`   | Latitude                   |
| `Longitude`  | Longitude                  |

---

## ANN MODEL

The Artificial Neural Network is implemented using **TensorFlow/Keras**.

### Model Workflow

```text
California Housing Dataset
          ↓
Train-Test Split
          ↓
Feature Standardization
          ↓
Input Layer
          ↓
Dense Hidden Layers
          ↓
Output Layer
          ↓
House Value Prediction
```

The input layer receives the 8 features, while the output layer produces a continuous predicted house value.

---

## ALGORITHM

1. Import the required Python libraries.
2. Load the California Housing Dataset from Scikit-learn.
3. Separate the input features and target variable.
4. Split the dataset into training and testing sets.
5. Standardize the input features using `StandardScaler`.
6. Build the ANN model using TensorFlow/Keras.
7. Compile the model with a suitable optimizer and loss function.
8. Train the model using the training dataset.
9. Predict house values using the trained model.
10. Evaluate the model using:

    * Mean Squared Error (MSE)
    * Mean Absolute Error (MAE)
    * Root Mean Squared Error (RMSE)

---

## EVALUATION METRICS

### Mean Squared Error (MSE)

MSE measures the average squared difference between the actual and predicted values.

### Mean Absolute Error (MAE)

MAE measures the average absolute difference between actual and predicted values.

### Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and represents the prediction error in the same scale as the target variable.

---

## RESULTS

The trained ANN model was evaluated on the test dataset using MSE, MAE, and RMSE.

| Metric |         Result |
| ------ | -------------: |
| MSE    | Add your value |
| MAE    | Add your value |
| RMSE   | Add your value |

> **Note:** Replace the values above with the actual values obtained from your Google Colab/Jupyter Notebook.

---

## OUTPUT

### Code Screenshot

Add the screenshot of the implemented ANN code here.

```text
[Insert Code Screenshot]
```

### Output Screenshot

Add the screenshot showing the model output and evaluation metrics here.

```text
[Insert Output Screenshot]
```

---

## PROJECT STRUCTURE

```text
ANN-Regression/
│
├── ANN_Regression.ipynb
├── README.md
└── screenshots/
    ├── code.png
    └── output.png
```

---

##  KEY CONCEPTS USED

* Artificial Neural Networks
* Regression
* TensorFlow
* Keras
* Data Preprocessing
* Feature Standardization
* Train-Test Split
* Dense Layers
* Backpropagation
* Model Training
* Regression Evaluation Metrics

---

## CONCLUSION

An Artificial Neural Network was successfully implemented using **TensorFlow/Keras** for predicting median house values using the California Housing Dataset. The input features were standardized before training, and the trained model was evaluated using **MSE, MAE, and RMSE**. This experiment demonstrates how ANN models can be applied effectively to regression problems.

