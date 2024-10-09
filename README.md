# BrainTumorMRI

Introduction
This project focuses on the classification of brain tumors using MRI images. The objective is to develop a deep learning model capable of accurately distinguishing between different classes of brain tumors. The dataset used comprises labeled MRI images, which allows us to train and validate our model effectively.

Methodology
Data Preparation
Data Loading:

We utilize the ImageFolder class from torchvision.datasets to load our training and validation datasets from specified directories.
The datasets consist of MRI images categorized into different classes, corresponding to various tumor types.
Data Transformation:

Images are resized to a uniform size of 224x224 pixels.
A series of transformations are applied, including random rotations, flips, and normalization to enhance the model's robustness and accuracy.
Data Visualization:

We visualize the distribution of images across classes using seaborn, providing insights into class balance and potential biases in the dataset.
Model Architecture
We employ the ResNet-18 architecture for this classification task. This model, known for its residual connections, is particularly effective in training deep neural networks by alleviating the vanishing gradient problem.

Training Process
Loss Function and Optimizer:

The model is trained using the Cross Entropy Loss function, suitable for multi-class classification tasks.
We utilize the Adam optimizer, which adapts the learning rate during training for improved convergence.
Training Loop:

The training process is carried out over 25 epochs, where both training and validation losses and accuracies are recorded for analysis.
After each epoch, the model's performance is evaluated on the validation set, and the best model (with the highest validation accuracy) is saved.
Performance Evaluation
After training, we plot the training and validation losses and accuracies to visualize the model's performance over epochs.
The final validation accuracy achieved by the model is approximately 96.49%, indicating a high level of confidence in the classification of MRI images.


Random Image Predictions
To demonstrate the model's effectiveness, we randomly select images from the validation dataset and display both the actual and predicted labels. This allows us to qualitatively assess the model's performance.
