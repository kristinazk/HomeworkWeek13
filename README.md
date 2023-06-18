# HomeworkWeek13

## General Overview

This repository contains two models classifying 10 different types of animals: cat, dog, squirrel, chicken, horse, cow, spider, butterfly, sheep, elephant.

In order to complete the task, techniques such as input normalization, dropout, data augmentation, transfer learning were used.

**The size of all the images is fixed to (224, 224) + (3,) (rgb).**

## Dataset Description

The [Animals-10](https://www.kaggle.com/datasets/alessiocorrado99/animals10) dataset used for training and validation was taken from Kaggle. It contains more than 26.000 images of different sizes.

The test dataset (AnimalTest.zip) was created manually from different Kaggle datasets. It contains all the 10 classes our models are able to classify.

## Models Description

The first model (animal_classification.ipynb) uses [MobileNet](https://keras.io/api/applications/mobilenet/) as a base, whereas the second model (train.ipynb) uses [EfficientNetB0](https://keras.io/api/applications/efficientnet/#efficientnetb0-function).

Additionally, in both models GlobalAveragePooling is applied in order to then fit the results to dense layers.

The first model's accuracy (tested on data taken from Animals-10) is **~96%**.

The second model's accuracy (tested on the dataset created manually) is **~97%**.

**NOTE** The class names of Animals-10 dataset are different from the ones used in the dataset created manually, since the class names in Animals-10 are in Italian.

translate = {"cane": "dog", "cavallo": "horse", "elefante": "elephant", "farfalla": "butterfly", "gallina": "chicken", "gatto": "cat", "mucca": "cow", "pecora": "sheep", "scoiattolo": "squirrel", "dog": "cane", "cavallo": "horse", "elephant" : "elefante", "butterfly": "farfalla", "chicken": "gallina", "cat": "gatto", "cow": "mucca", "spider": "ragno", "squirrel": "scoiattolo"}

