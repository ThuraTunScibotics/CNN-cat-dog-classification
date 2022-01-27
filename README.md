# CNN-cat-dog-classification

** Updated with dropout

## Project Description
The project is implementation of cat and dog classification using Convolution Neural Networks (CNN). We can predict any images in the `datasets/single_prediction` directory, and it is need to put any cat and dog image that we want to predict in this directory.

## Dataset
In the training_set & test_set of the dataset, 
* there are 4000 images in the training_set for each cat and dog category, 
* there are 1000 images in the test_set for each cat and dog category
The dataset is provided in the repository

## Model Architecture of CNN

`(64, 64, 3)` -> `Convolution` ->  `MaxPooling` -> `Convolution` -> `MaxPooling` ->  `Flattening` -> `Dense` -> `Dropout` -> `Dense` -> `Dropout` -> SIGMOID

* Convolution with `filters=32` and `kernel_size=3` and `activations='relu'`
* MaxPooling with `pool_size=2` and `strides=2`
* The first two Dense layer with `units=128` and `activation='relu'`
* Dropout each first two layer (UPDATE!!!)
* The final Dense layer with `units=1` and `activation=SIGMOID `


## Predicted result
When we predict on our custom images, the result is as follow.

**Without dropout
<img src="images/cat-dog-predict-result.png">
