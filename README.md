
# MNIST Digit Classification with Keras

This notebook demonstrates how to build and train a simple neural network using Keras and TensorFlow to classify handwritten digits from the MNIST dataset.

## 1. Import Libraries
Imports necessary libraries from TensorFlow and Keras for building the neural network.

## 2. Load and Explore Data
Loads the MNIST dataset, which consists of 60,000 training images and 10,000 testing images of handwritten digits. Initial exploration of data shape and an example image is performed.

## 3. Preprocess Data
The pixel values of the images are normalized to a range between 0 and 1 by dividing by 255. This helps in faster and more stable training of the neural network.

## 4. Build the Model
A sequential Keras model is defined with the following layers:
*   **Flatten**: Converts the 28x28 2D image arrays into a 1D vector of 784 pixels.
*   **Dense (128 units, ReLU activation)**: A hidden layer with 128 neurons and Rectified Linear Unit (ReLU) activation function.
*   **Dense (10 units, Softmax activation)**: The output layer with 10 neurons (one for each digit 0-9) and a softmax activation function to output probability distributions over the classes.

## 5. Compile the Model
The model is compiled with:
*   **Loss Function**: `sparse_categorical_crossentropy` (suitable for integer labels).
*   **Optimizer**: `Adam` (an efficient stochastic gradient descent algorithm).

## 6. Train the Model
The model is trained on the `X_train` and `y_train` data for 10 epochs. A validation split of 20% is used to monitor performance on unseen data during training.

## 7. Evaluate the Model
After training, the model makes predictions on the `X_test` data. The predicted probabilities are converted to class labels, and the accuracy score is calculated against the true labels (`y_test`).
The final accuracy achieved is 97.87%
