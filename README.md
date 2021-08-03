# FYP_Cityu

Objectives:
1. Getting Chinese White Dolphins images from the database;

2. Training the computer vision model to recognize the Chinese White Dolphins;

3. Integrate all the things into a single API for the web-application platform to get the classification results;

Deliverables:
1. Provide an application for people to recognize the Chinese White Dolphin individuals;

Google drive link:
https://drive.google.com/drive/folders/1YEocdFUR7yApmAArTpi9pE-3A7QCR14l

Setup/Demo Instructions:
Please install Tensorflow 1.17 and Python 3.6 for following the scripts and the API.

The object detection API Python script used to train a fin detector is saved in \TensorFlow_with_Colab_tutorial.ipynb

The fin detector model is saved in the \saved_model\saved_model.pb

The script that is used to extract the fin part of the Chinese white dolphin is saved in \object_detection_tutorial_extractfins.ipynb

The trained triplet-loss model is saved in \TrainingTripletModel\TripletModel\

The divided training dataset and testing dataset for training the triplet loss model are saved in \TrainingTripletModel\data2 and \TrainingTripletModel\lfw respectively.

The script used to evaluate the triplet-loss model is saved in \TrainingTripletModel\validate_on_lfw.py

The trained classifier is saved in \TrainingClassifier\output\

The script used to train and test the classifier is in \TrainingClassifier\classifier.py

The training dataset and testing dataset for training and testing the classifier are saved in \TrainingClassifier\train2 and \TrainingClassifier\test2 respectively.

Users can try the following command to use the trained classifier to show the classification result on the testing dataset:

CLASSIFY /Test2 ../TrainingTripletModel/TripletModel/ /output/result2.pkl 

The script that is used to predict the class of a single input dolphin image is in \predict.py

Users can try the following command to use the API to show the classification result for a single dolphin input:

/Test2/01/01_4.jpg  ../TrainingTripletModel/TripletModel /output/result2.pkl 
