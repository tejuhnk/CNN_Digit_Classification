# 🧠 MNIST Handwritten Digit Classification
### A Comparative Study of Perceptron, Artificial Neural Networks (ANN), and Convolutional Neural Networks (CNN)

Exploring how different neural network architectures learn to recognize handwritten digits using the MNIST dataset.

## 📌 Project Overview

Handwritten digit recognition is a classic computer vision problem in which a machine learning model identifies digits from images.

This project implements and compares three neural network approaches — **Perceptron, ANN, and CNN** — to understand how model architecture affects classification performance on 28 × 28 grayscale digit images.

Rather than training a single model, this project evaluates multiple approaches using test accuracy, training and validation curves, prediction visualizations, and a confusion matrix.

## ✨ Key Features

- 🧠 Implementation of Perceptron, ANN, and CNN models
- 🖼️ MNIST handwritten digit image preprocessing
- ⚙️ Neural network training using TensorFlow/Keras
- 📊 Training and validation accuracy visualization
- 📉 Training and validation loss analysis
- 🔍 Side-by-side prediction comparison across models
- 🎯 CNN confusion matrix for classification error analysis
- 📈 Final test accuracy comparison across all three architectures

## 🗂️ Dataset

**Dataset:** MNIST Handwritten Digits

The dataset contains grayscale images of handwritten digits from 0 to 9.

| Property | Description |
|---|---|
| Image dimensions | 28 × 28 pixels |
| Image channels | 1 (grayscale) |
| Classes | 10 (digits 0–9) |
| Input features | 784 pixel values per image |
| Label | Digit represented by the image |

The notebook loads the training and test datasets from `mnist_train.csv` and `mnist_test.csv`.

Ensure these files are available in the expected working directory before running the notebook. Add their download/source link here if you redistribute or reference an external copy.

## 🏗️ Model Architectures

### 1. Perceptron

A simple neural network baseline that flattens the image and directly predicts probabilities for the ten digit classes.

- Flatten layer
- Dense output layer with 10 neurons
- Softmax activation
- SGD optimizer

### 2. Artificial Neural Network (ANN)

A fully connected neural network that learns nonlinear patterns from pixel values.

**Architecture:**

`784 → 128 → 64 → 10`

- Flatten layer
- Dense layer with 128 neurons and ReLU activation
- Dense layer with 64 neurons and ReLU activation
- Output layer with 10 neurons and Softmax activation
- Adam optimizer

### 3. Convolutional Neural Network (CNN)

A CNN that learns spatial patterns and visual features from handwritten digit images through convolution and pooling operations.

**Architecture:**

`Input → Conv2D(32) → MaxPooling → Conv2D(64) → MaxPooling → Flatten → Dense(128) → Dropout(0.5) → Output(10)`

- Two convolutional layers with ReLU activation
- Two max-pooling layers
- Flatten layer
- Dense layer with 128 neurons
- Dropout regularization with a rate of 0.5
- Softmax output layer with 10 classes
- Adam optimizer

## ⚙️ Data Preprocessing

The notebook performs the following preprocessing steps:

1. Separates input pixel values from digit labels.
2. Converts pixel values to `float32`.
3. Normalizes pixel intensities from the range 0–255 to 0–1.
4. Reshapes images into 28 × 28 arrays for the baseline models.
5. Adds a channel dimension for CNN input.
6. Converts digit labels into one-hot encoded vectors.

## 🛠️ Technology Stack

- **Language:** Python
- **Deep Learning:** TensorFlow / Keras
- **Data Processing:** NumPy, Pandas
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning Utilities:** Scikit-learn
- **Environment:** Jupyter Notebook

## 🚀 Getting Started

### Prerequisites

Install Python and Jupyter Notebook, then install the required packages.

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/mnist-digit-classification.git
cd mnist-digit-classification
```

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn tensorflow jupyter
```

### 3. Add the dataset

Place the following CSV files in the directory expected by the notebook:

```text
mnist_train.csv
mnist_test.csv
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `CNN.ipynb` and execute the cells in order.

## 📊 Model Evaluation

The notebook evaluates the models using:

- **Test Accuracy:** Measures the proportion of correctly classified digits.
- **Training vs. Validation Curves:** Tracks accuracy and loss across epochs.
- **Prediction Comparison:** Compares the predicted digits from all three models.
- **Confusion Matrix:** Visualizes correct predictions and misclassifications for the CNN.

A final bar chart compares the test accuracy of the Perceptron, ANN, and CNN models.

> **Results:** Run the notebook and record the actual test accuracy of each model here. Results depend on the dataset, training configuration, and execution environment.

| Model | Test Accuracy |
|---|---|
| Perceptron | Add measured result |
| ANN | Add measured result |
| CNN | Add measured result |

## 📁 Project Structure

```text
mnist-digit-classification/
├── CNN.ipynb
├── README.md
├── requirements.txt
├── mnist_train.csv
└── mnist_test.csv
```

The dataset files may be excluded from the repository if they are large or subject to redistribution restrictions. If excluded, document where to obtain them.

## 🔮 Future Improvements

- Experiment with different CNN architectures and filter sizes.
- Tune batch size, learning rate, and number of epochs.
- Add precision, recall, and F1-score comparisons.
- Evaluate individual misclassified digits.
- Save the trained model for reuse.
- Build an interactive application for handwritten digit prediction.

## 🎯 Learning Outcomes

Through this project, I explored:

- The differences between linear classification, fully connected networks, and convolutional neural networks.
- Image normalization and reshaping for deep learning.
- The role of convolution, pooling, and dropout.
- Training and validation performance analysis.
- Classification evaluation using confusion matrices and test accuracy.

## 👨‍💻 Author

**YOUR NAME**

GitHub: [YOUR_USERNAME](https://github.com/YOUR_USERNAME)

---

*Built as a hands-on deep learning project to explore neural network architectures and computer vision fundamentals.*
