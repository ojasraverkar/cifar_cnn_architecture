# Cifar_CNN_Architecture
This code implements a Convolutional Deep Learning model which classifies data from the CIFAR10 dataset.

## Data - preprocessing and loading images
Firstly, load the csv file with labels into a pandas dataframe.

Define a list with all the classes.

Use cv2 to resize and read the images and append them to respective list.

Convert the images and labels lists to numpy lists as any model based on tensorflow and keras works fastest on numpy lists.

## Model Specs

Conv2D (32 filters) - Convolution - Used to extract features like shapes

MaxPooling2D - Pooling - reduces size for fast processing

Dropout - Preventing overfitting by dropping some nodes

Batch Normalisation - Helps to converge and speed up training

Conv2D (64 filters) - Convolution - Extract more detailed features

MaxPooling2D - Pooling - reduces size again for faster processing

Flatten - Convert to 1D vector

Dense (128 units) - Fully connected - Patterns and relationship spotting

Dense (10 units) - Output Layer - Final classification

Use activation function - Relu for layers and Softmax for output layers.

## Model Training and EDA

Compile the model and add Early stopping to select the best epoch which gives the best results(accuracy and loss)

Fit the model and plot accuracy and loss using matplotlib.

Print Classification report as well.