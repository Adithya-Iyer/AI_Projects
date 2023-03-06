# Image Classification using CNN Architecture

This project is an image classification model using Convolution Neural Networks (CNN) in PyTorch.

### Dataset Information

* The data set (i.e. Fashion-MNIST) can be found here: https://github.com/zalandoresearch/fashion-mnist/tree/master/data/fashion 
* Information about this dataset can be found here: https://github.com/zalandoresearch/fashion-mnist 
* It consists of a training set of 60,000 examples and a test set of 10,000 examples. Each example is a 28x28 grayscale image, associated with a label from 10 classes.

### Steps Involved

1. Loading the data set
   - Please explore a few samples and visualize these images
2. Creating a validation set and preprocessing the images
   - Split the training data set to a training set (90% samples) and a validation set (10% samples) 
   - Convert the images and the targets into torch format for both training and validation data sets
3. Implementing CNNs using PyTorch
   - Define the architecture with just 2 convolutional layers to extract features from the images, then use a fully connected dense layer to classify those features into their respective categories (i.e. two Conv2d layers and a linear layer) 
   - Train the model for 25 epochs and show the validation losses by printing in console 
   - See that the validation loss is decreasing as epoch increases Visualize the training and validation losses by plotting them 
   - Show the accuracy of the model on the training and validation set
4. Generating predictions for the test set
   - Load the test images 
   - Do the pre-processing steps on these images similar to what you did for the training images 
   - Generate predictions for the test set

## LeNet-5 CNN Architecture

The example codes in the following link were written in TensorFlow, but PyTorch has been used in this project. Refer to the link given for the reference for step-by-step instructions on implementing LeNet-5 Architecture: https://medium.datadriveninvestor.com/lenet-5-a-classic-cnn-architecture-c87d0b03560d
