# ARABIC-NUMBER-PREDICTION-USING-CNN
# CNN Image Classification Using TensorFlow and Keras

## Project Overview

This project implements a **Convolutional Neural Network (CNN)** to classify grayscale images using TensorFlow and Keras. The dataset contains 28 × 28 pixel images, with each image represented by 784 pixel values and an associated class label.

The objective is to preprocess the image data, build and train a CNN for 5 epochs, evaluate its performance on a separate test dataset, and visualize sample images alongside their actual and predicted labels.

## Objectives

- Load training and testing image data from CSV files.
- Select a random sample of 5,000 training images.
- Reshape pixel data into 28 × 28 grayscale images.
- Normalize pixel values to the range 0–1.
- Build and train a CNN using Keras.
- Evaluate model performance using test accuracy.
- Visualize five test images with their true and predicted labels.

## Dataset

The project uses four CSV files:

- `csvTrainImages 60k x 784.csv` — training images.
- `csvTrainLabel 60k x 1.csv` — training labels.
- `csvTestImages 10k x 784.csv` — testing images.
- `csvTestLabel 10k x 1.csv` — testing labels.

Each image contains 784 pixel values, corresponding to a 28 × 28 grayscale image.

For efficient training, a random sample of 5,000 images is selected from the training dataset. The separate test dataset contains 10,000 images.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- TensorFlow
- Keras

## Data Preprocessing

The following preprocessing steps are performed:

1. Load image and label data from CSV files.
2. Randomly select 5,000 training images while preserving their corresponding labels.
3. Reshape each image from 784 pixel values into a 28 × 28 × 1 array.
4. Convert pixel values to floating-point numbers.
5. Normalize pixel values by dividing by 255.
6. Use the provided training and testing datasets for model development and evaluation.

## CNN Architecture

The model follows the required architecture:

| Layer | Configuration |
|---|---|
| Input | 28 × 28 × 1 |
| Convolutional Layer | 32 filters, 3 × 3 kernel, ReLU |
| Max Pooling | MaxPooling2D |
| Convolutional Layer | 64 filters, 3 × 3 kernel, ReLU |
| Max Pooling | MaxPooling2D |
| Flatten | Converts feature maps into a vector |
| Dense Layer | 64 neurons, ReLU |
| Output Layer | `n_classes` neurons, Softmax |

The convolutional layers extract image features, while the pooling layers reduce spatial dimensions. The dense layers use these features to predict the image class.

## Model Training

The CNN is compiled using:

- **Optimizer:** Adam
- **Loss Function:** Sparse Categorical Crossentropy
- **Evaluation Metric:** Accuracy
- **Epochs:** 5
- **Batch Size:** 32

A validation split of 10% of the sampled training data is used to monitor model performance during training.

## Model Evaluation

The trained model is evaluated on the separate test dataset.

The evaluation reports:

- Test loss
- Test accuracy

The notebook also displays five test images with their actual labels and CNN-predicted labels, allowing visual inspection of the model's predictions.

**Test Accuracy:** Add the verified accuracy obtained after successfully running the corrected notebook from beginning to end.

## Results and Observations

This project demonstrates how CNNs can learn spatial features from grayscale images and use them for multiclass classification.

The final test accuracy indicates how well the model generalizes to unseen test images. Comparing actual and predicted labels helps identify correct predictions and potential classification errors.

## How to Run the Project

1. Clone or download this repository.
2. Open the notebook in Jupyter Notebook or Google Colab.
3. Upload the four dataset CSV files.
4. Update file paths if necessary.
5. Run all notebook cells in order.
6. Review the training history, test accuracy, and sample prediction visualizations.

## Future Improvements

- Train on the full training dataset.
- Experiment with different filter sizes and numbers of convolutional layers.
- Compare performance across different batch sizes and optimizers.
- Add a confusion matrix and classification report.
- Save the trained model for future image predictions.

## Conclusion

This project demonstrates an end-to-end image classification workflow using a CNN, from CSV-based data loading and image preprocessing to model training, evaluation, and visualization. It provides practical experience with deep learning, image feature extraction, and multiclass classification using TensorFlow and Keras.
