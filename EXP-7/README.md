
# Autoencoder for Dimensionality Reduction and Feature Learning

## Aim
To implement and train a simple Autoencoder for dimensionality reduction and feature learning by compressing input data into a lower-dimensional representation and reconstructing the original data from the learned features.

## Technologies Used
- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- GitHub

## Dataset
**MNIST Handwritten Digits Dataset**

- Contains 70,000 grayscale handwritten digit images.
- Each image has a size of 28 × 28 pixels.
- Training samples: 60,000
- Testing samples: 10,000
- Pixel values are normalized between 0 and 1.

## Autoencoder Architecture

The Autoencoder consists of three main components:

1. **Encoder:** Compresses the input data from 784 to 128 features.
2. **Bottleneck:** Reduces the representation to 32 important features.
3. **Decoder:** Reconstructs the original input from the compressed representation.

| Layer | Neurons |
|---|---:|
| Input Layer | 784 |
| Encoder | 128 |
| Bottleneck | 32 |
| Decoder | 128 |
| Output Layer | 784 |

## Implementation Steps

### Part A: Dataset Preparation
- Load the MNIST dataset.
- Explore the dataset and display sample images.
- Normalize pixel values between 0 and 1.
- Reshape images into one-dimensional vectors.
- Prepare training and testing datasets.

### Part B: Implementing the Autoencoder
- Define the input layer.
- Build the Encoder and Decoder using Dense layers.
- Introduce a 32-neuron bottleneck layer.
- Compile the model using Adam optimizer and Mean Squared Error (MSE).
- Display the model summary.

### Part C: Model Training and Performance Evaluation
- Train the Autoencoder using the MNIST dataset.
- Record training and validation loss.
- Evaluate the model using test data.
- Calculate reconstruction MSE.
- Plot training and validation loss.
- Compare original and reconstructed images.

### Part D: Dimensionality Reduction and Feature Visualization
- Extract latent-space representations using the Encoder.
- Compare original and compressed dimensions.
- Visualize latent features using PCA.
- Reconstruct selected test images using the Decoder.
- Analyze reconstruction quality and dimensionality reduction.
- Upload the notebook to GitHub.

## Results

- Original input dimensions: 784 features.
- Compressed dimensions: 32 features.
- Dimensionality reduction: Approximately 95.92%.
- PCA was used to visualize the learned features in two dimensions.
- The Decoder reconstructed images from the compressed representations.

## Conclusion

The Autoencoder successfully learned a compact representation of the MNIST handwritten digit images. It reduced the input dimensions from 784 to 32 while retaining important features for reconstruction. The experiment demonstrates the use of Autoencoders for dimensionality reduction, feature learning and image reconstruction.

