# Assamese Number Recognition

A deep learning project for recognizing Assamese handwritten digits using TensorFlow and Keras.

This project trains a neural network model on Assamese number images and predicts handwritten Assamese digits from input images.

## Project Overview

The notebook builds and trains a digit classification model using:

* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib

The model processes image datasets stored in Google Drive and performs handwritten digit recognition for Assamese numbers.

## Features

* Image dataset loading using TensorFlow
* Automatic training and validation split
* Image normalization
* Neural network training
* Accuracy and loss visualization
* Prediction on custom handwritten images
* Confidence score generation

## Technologies Used

* Python
* TensorFlow
* Keras
* Google Colab
* NumPy
* Pandas
* Matplotlib

## Project Structure

```text
Assamese number recognisation.ipynb
```

The notebook contains:

1. Dataset loading
2. Data preprocessing
3. Model creation
4. Model training
5. Accuracy and loss plotting
6. Image prediction testing

## Dataset

The dataset is loaded from Google Drive using:

```python
from google.colab import drive
drive.mount('/content/drive')
```

Images are loaded using:

```python
tf.utils.image_dataset_from_directory()
```

### Image Specifications

* Image size: 28 × 28
* Batch size: 32
* Validation split: 20%

## Model Architecture

The neural network uses:

```python
Flatten Layer
Dense Layer (784 neurons, ReLU)
Dense Output Layer (10 neurons, Softmax)
```

### Output Classes

The model predicts digits from 0 to 9.

## Training

The model is trained using:

```python
model.compile(
    loss='sparse_categorical_crossentropy',
    optimizer='adam',
    metrics=['accuracy']
)
```

Training configuration:

* Epochs: 10
* Optimizer: Adam
* Loss Function: Sparse Categorical Crossentropy

## Accuracy Visualization

The notebook generates:

* Accuracy graph
* Validation accuracy graph
* Loss graph

These graphs help evaluate model performance during training.

## Prediction Workflow

A custom image is loaded and processed before prediction:

```python
img = load_img(img_path, target_size=(28, 28))
```

The image is:

1. Converted to array
2. Normalized
3. Expanded into batch format
4. Passed into the trained model

The model outputs:

* Predicted digit
* Probability scores
* Confidence percentage

## How to Run

### Requirements

Install required libraries:

```bash
pip install tensorflow numpy pandas matplotlib
```

### Run in Google Colab

1. Upload the notebook to Google Colab
2. Upload dataset to Google Drive
3. Update dataset path
4. Run all notebook cells

## Example Workflow

```text
Dataset → Preprocessing → Training → Evaluation → Prediction
```

## Future Improvements

* Use Convolutional Neural Networks (CNN)
* Increase dataset size
* Add real time digit recognition
* Improve model accuracy
* Deploy as a web application
* Add Assamese character recognition

## Learning Outcomes

This project demonstrates:

* Image classification fundamentals
* Neural network training
* Dataset preprocessing
* Deep learning workflows
* Model evaluation techniques
* Handwritten digit recognition

## Author

Rajmohan Hazowary
