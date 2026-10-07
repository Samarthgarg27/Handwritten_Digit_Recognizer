# Handwritten_Digit_Recognizer
A CNN-based handwritten digit recognition system trained on the MNIST dataset. The project includes image preprocessing, CNN model training, evaluation, prediction, accuracy/loss visualization, and confusion matrix analysis using TensorFlow and Keras.
# Handwritten Digit Recognizer

## Overview

Handwritten Digit Recognizer is a deep learning project that uses a **Convolutional Neural Network (CNN)** to recognize handwritten digits from **0 to 9**.

The model is trained using the **MNIST dataset**, which contains thousands of handwritten digit images. The project demonstrates how image preprocessing, CNNs, model training, and evaluation can be used for image classification.

## Features

* Handwritten digit classification from 0 to 9
* CNN-based image classification
* MNIST dataset
* Image normalization and preprocessing
* Model training and validation
* Accuracy and loss visualization
* Confusion matrix analysis
* Classification report
* Prediction of individual handwritten digits
* Analysis of incorrect predictions
* Trained model saving

## Technologies Used

* **Python**
* **TensorFlow**
* **Keras**
* **NumPy**
* **Matplotlib**
* **Scikit-learn**
* **Seaborn**
* **Google Colab**

## Dataset

The project uses the **MNIST handwritten digit dataset**.

The dataset contains:

* **60,000** training images
* **10,000** testing images
* Image size: **28 × 28 pixels**
* Grayscale images
* **10 classes:** 0, 1, 2, 3, 4, 5, 6, 7, 8, 9

## How the Model Works

The input image goes through the following pipeline:

```text
MNIST Image
     ↓
Image Preprocessing
     ↓
Normalization
     ↓
Convolutional Layer
     ↓
Max Pooling
     ↓
Convolutional Layer
     ↓
Max Pooling
     ↓
Flatten
     ↓
Dense Layer
     ↓
Dropout
     ↓
Output Layer
     ↓
Predicted Digit (0-9)
```

## CNN Architecture

The model consists of:

1. **Conv2D Layer**

   * 32 filters
   * 3 × 3 kernel
   * ReLU activation

2. **MaxPooling Layer**

   * 2 × 2 pool size

3. **Conv2D Layer**

   * 64 filters
   * 3 × 3 kernel
   * ReLU activation

4. **MaxPooling Layer**

   * 2 × 2 pool size

5. **Flatten Layer**

6. **Dense Layer**

   * 128 neurons
   * ReLU activation

7. **Dropout Layer**

   * Dropout rate: 0.5

8. **Output Layer**

   * 10 neurons
   * Softmax activation

## Data Preprocessing

Before training, the images are normalized from the original pixel range:

```text
0 - 255
```

to:

```text
0 - 1
```

The images are also reshaped to include a channel dimension required by the CNN:

```text
28 × 28 → 28 × 28 × 1
```

## Model Training

The model is trained using:

* **Optimizer:** Adam
* **Loss Function:** Sparse Categorical Crossentropy
* **Epochs:** 10
* **Batch Size:** 64
* **Validation Split:** 10%

## Evaluation

The trained model is evaluated on the MNIST test dataset.

The project uses:

* Test accuracy
* Test loss
* Confusion matrix
* Precision
* Recall
* F1-score
* Incorrect prediction analysis

A basic CNN architecture can achieve approximately **98–99% accuracy** on the MNIST test dataset.

## Results

The project generates visualizations for:

### Training and Validation Accuracy

The accuracy graph shows how the model's performance changes during training.

### Training and Validation Loss

The loss graph helps understand whether the model is learning effectively and whether overfitting is occurring.

### Confusion Matrix

The confusion matrix shows how accurately the model classifies each digit and which digits are commonly confused with each other.

### Sample Predictions

The model can display handwritten images along with:

```text
Predicted Digit
Actual Digit
```

## Project Structure

```text
Handwritten-Digit-Recognizer/
│
├── Handwritten_Digit_Recognizer.ipynb
├── handwritten_digit_cnn.keras
├── README.md
└── requirements.txt
```

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Handwritten-Digit-Recognizer.git
```

Navigate to the project directory:

```bash
cd Handwritten-Digit-Recognizer
```

Install the required libraries:

```bash
pip install tensorflow numpy matplotlib scikit-learn seaborn
```

## Running the Project

The easiest way to run this project is using **Google Colab**.

1. Open the `.ipynb` notebook.
2. Upload it to Google Colab.
3. Run the cells from top to bottom.
4. The MNIST dataset will be loaded automatically.
5. Train the CNN model.
6. Evaluate the model.
7. Test handwritten digit predictions.

## Example

The model takes a handwritten digit image as input:

```text
Input Image
     ↓
     CNN
     ↓
Prediction
     ↓
Digit: 7
Confidence: 99%+
```

## Learning Outcomes

Through this project, I learned:

* Basics of image classification
* How CNNs work
* Image preprocessing
* Normalization of image data
* Convolution and pooling
* Model training and validation
* Model evaluation
* Confusion matrix analysis
* Making predictions using a trained CNN
* Saving and reusing a trained deep learning model

## Future Improvements

The project can be further improved by:

* Adding a web interface for digit prediction
* Allowing users to draw digits on a canvas
* Deploying the model using Streamlit or Flask
* Adding real-time digit recognition
* Experimenting with different CNN architectures
* Comparing CNN performance with other machine learning algorithms

## Conclusion

This project demonstrates how a **Convolutional Neural Network** can be used to classify handwritten digits effectively. Using the MNIST dataset, the model learns visual patterns from handwritten digits and predicts the correct digit from 0 to 9.

The project provides a practical introduction to **deep learning, computer vision, CNNs, and image classification**.
