# Transfer Learning for Image Classification

## 1. Aim

To implement transfer learning using pre-trained vision models for image recognition and evaluate their performance on a real-world image dataset.

---

## 2. Objectives

* Understand the concept of transfer learning.
* Apply a pre-trained vision model for image classification.
* Use ResNet-50 for transfer learning.
* Freeze the feature extraction layers of the pre-trained model.
* Replace the final classification layer according to the dataset classes.
* Train and evaluate the transfer learning model.
* Use a pre-trained vision model from Hugging Face.
* Compare predictions from the Hugging Face model and the transfer learning model.
* Document the experiment using GitHub.

---

## 3. Dataset

### Intel Image Classification Dataset

The Intel Image Classification dataset is obtained from Kaggle and contains images belonging to six classes:

1. Buildings
2. Forest
3. Glacier
4. Mountain
5. Sea
6. Street

The dataset is downloaded directly from Kaggle using **KaggleHub**, without requiring the traditional `kaggle.json` file.

---

## 4. Software Requirements

* Python
* TensorFlow / Keras
* Google Colab
* KaggleHub
* Hugging Face Transformers
* PyTorch
* NumPy
* Matplotlib
* GitHub

---

## 5. Technologies Used

| Technology                | Purpose                                   |
| ------------------------- | ----------------------------------------- |
| Python                    | Programming language                      |
| TensorFlow/Keras          | Model development and training            |
| ResNet-50                 | Transfer learning model                   |
| KaggleHub                 | Dataset download                          |
| Hugging Face Transformers | Pre-trained vision model                  |
| PyTorch                   | Running the Hugging Face ViT model        |
| NumPy                     | Numerical operations                      |
| Matplotlib                | Visualization                             |
| GitHub                    | Version control and project documentation |

---

# 6. Implementation

## Task A: Dataset Preparation

The Intel Image Classification dataset is downloaded from Kaggle using KaggleHub.

The images are loaded using TensorFlow's `image_dataset_from_directory()` function.

The images are resized to:

```text
224 × 224 pixels
```

The dataset is divided into:

* **80% Training**
* **20% Validation**
* **Separate Test Dataset**

The six class labels are automatically obtained from the folder names.

---

## Task B: Implementing Transfer Learning

A pre-trained **ResNet-50** model with ImageNet weights is used.

The original classification layer is removed using:

```python
include_top=False
```

A new classification layer is added with six output classes corresponding to the Intel dataset.

The feature extraction layers are frozen:

```python
base_model.trainable = False
```

A Global Average Pooling layer and a Dense layer with softmax activation are added for classification.

The model is compiled using:

* **Optimizer:** Adam
* **Loss:** Sparse Categorical Crossentropy
* **Metric:** Accuracy

---

## Task C: Model Training and Performance Evaluation

The transfer learning model is trained using the training dataset and validated using the validation dataset.

The following performance measures are recorded:

* Training Accuracy
* Validation Accuracy
* Training Loss
* Validation Loss
* Test Accuracy

Two graphs are generated:

### Accuracy vs Epoch

This graph shows the changes in training and validation accuracy over the training epochs.

### Loss vs Epoch

This graph shows the changes in training and validation loss over the training epochs.

The final test accuracy is used to evaluate the model's performance on unseen images.

---

## Task D: Using Hugging Face Pre-trained Models

A pre-trained **Vision Transformer (ViT)** model is loaded from Hugging Face:

```text
google/vit-base-patch16-224
```

The model is used to classify sample images from the test dataset.

The predictions from the Hugging Face model are compared with the predictions from the ResNet-50 transfer learning model.

The comparison demonstrates the difference between:

* A model specifically trained for the six Intel image classes.
* A general-purpose pre-trained ImageNet vision model.

---

# 7. Model Architecture

The transfer learning model follows this structure:

```text
Input Image
    ↓
224 × 224 × 3
    ↓
Preprocessing
    ↓
Pre-trained ResNet-50
    ↓
Frozen Feature Extraction Layers
    ↓
Global Average Pooling
    ↓
Dense Layer
    ↓
Softmax
    ↓
6 Classes
```

---

# 8. Results

The model performance is recorded after training.

| Metric              | Result                 |
| ------------------- | ---------------------- |
| Training Accuracy   | [Enter obtained value] |
| Validation Accuracy | [Enter obtained value] |
| Training Loss       | [Enter obtained value] |
| Validation Loss     | [Enter obtained value] |
| Test Accuracy       | [Enter obtained value] |

> **Note:** Replace the values above with the actual values obtained from Google Colab after running the experiment.

---

# 9. Observations

* Transfer learning reduces the amount of training required compared to training a CNN from scratch.
* The pre-trained ResNet-50 model can reuse useful visual features learned from ImageNet.
* Freezing the feature extraction layers reduces the number of trainable parameters.
* The model can achieve good classification performance with fewer training epochs.
* The validation and training curves help to understand the learning behavior of the model.
* The Hugging Face Vision Transformer provides an easy way to experiment with a pre-trained vision model.
* Predictions from the Hugging Face model may differ from ResNet-50 because the models were trained for different classification label sets.

---

# 10. Advantages of Transfer Learning

* Requires less training time.
* Requires fewer computational resources.
* Works effectively with smaller datasets.
* Provides useful pre-learned image features.
* Can achieve good accuracy with fewer epochs.
* Reduces the need to train a complete CNN from scratch.

---

# 11. Conclusion

Transfer learning was successfully implemented using a pre-trained ResNet-50 model for Intel Image Classification. The feature extraction layers were frozen and a new classification layer was added for the six target classes. The model was trained and evaluated using training, validation, and test datasets. Accuracy and loss graphs were used to analyze the model's performance. A pre-trained Vision Transformer from Hugging Face was also used for sample image classification and its predictions were compared with the ResNet-50 model. The experiment demonstrates that transfer learning provides an efficient approach for developing image classification models using pre-trained knowledge.

---

# 12. Future Enhancements

* Fine-tune selected layers of ResNet-50 for improved accuracy.
* Compare ResNet-50 with other pre-trained architectures.
* Use data augmentation to improve generalization.
* Experiment with different learning rates and optimizers.
* Evaluate additional Hugging Face vision models.

---

# 13. GitHub

The complete Google Colab notebook, code, results, graphs, and documentation are maintained in this GitHub repository.

**Repository:**
[Paste your GitHub repository link here]

---

## 14. Key Questions and Answers

### 1. What are the advantages of transfer learning compared to training a CNN from scratch?

Transfer learning uses knowledge learned from a large dataset, reducing training time and computational requirements. It can provide good accuracy with less training data and fewer epochs.

### 2. Why are pre-trained models able to achieve higher accuracy with fewer training epochs?

Pre-trained models already contain useful features such as edges, textures, shapes, and patterns. Therefore, they do not need to learn these basic features from the beginning.

### 3. Compare the performance of the transfer learning model with the CNN implemented in the previous experiment.

The transfer learning model generally achieves better accuracy and converges faster than a CNN trained from scratch because it uses previously learned features.

### 4. What is the purpose of freezing layers during transfer learning?

Freezing layers preserves the learned features of the pre-trained model and prevents their weights from being changed during initial training. It also reduces the number of trainable parameters and training time.

### 5. How can Hugging Face simplify the deployment and experimentation of vision models?

Hugging Face provides access to many ready-to-use pre-trained vision models and processors. This allows developers to load, test, and experiment with advanced models using relatively little code.

