# Face Mask Detection Project
![FaceMaskDetection](https://github.com/vishalrathourr/Face-Mask-Detection/assets/126953378/488f3e19-95c8-4355-913a-5ee203a3d3f8)

## Overview

This project is aimed at creating a real-time face mask detection system using machine learning with Python. It uses OpenCV for image processing, Haar Cascade Classifier for face detection, and a Support Vector Machine (SVC) for classification. The primary objective is to determine whether a person is wearing a mask or not from a webcam feed.

## Project Structure

The project is organized into two main parts, implemented in two separate Jupyter notebooks:

### Notebook 1: Data Collection Using Webcam

In this notebook, we collect data for training and testing the face mask detection model. The following steps are taken:

1. **Image Capture:** We utilize the computer's webcam to capture continuous images of individuals with and without masks. A total of 1000 images are collected for each category.
   
2. **Data Storage:** The captured images are stored as NumPy arrays in two separate files:
    - `with_mask.npy`: Contains images of people wearing masks.
    - `without_mask.npy`: Contains images of people without masks.
   
3. **Face Detection:** We employ the Haar Cascade Classifier (`haarcascade_frontalface_default.xml`) to detect faces within the images.

### Notebook 2: Model Training and Real-Time Detection

In this notebook, we train a Support Vector Machine (SVM) classifier to distinguish between images with masks and images without masks. The process includes the following steps:

1. **Data Preparation:** We load and preprocess the data from the previously generated NumPy arrays. This includes resizing the images and converting them to grayscale.

2. **Dimensionality Reduction:** Principal Component Analysis (PCA) is applied to reduce the dimensionality of the image data.

3. **Model Training:** We train an SVM classifier using the preprocessed data.

4. **Real-Time Detection:** We create a real-time face mask detection system using the trained SVM model. The webcam feed is processed in real-time, and the system labels the detected faces as either <font color="green">Mask</font> or <font color="red">No Mask</font>



<font color="red">**NOTE:** In this project I got the accuracy score 1.0 which is the case of overfitting that is not good in the machine learning model. Currently I could not resolve this by doing several trials If you how to do this please suggest me.</font>
