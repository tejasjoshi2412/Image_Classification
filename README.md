# Image_Classification

The project is based on the Intel Image Classification Dataset available of Kaggle. The Dataset includes the pictures of Buildings, Mountains, Glaciers, Street, Forest and Sea.

Libraries used :
1. Opencv
2. Python Imaging Library (PIL)
3. Numpy
4. OS
5. Tensorflow
6. Keras
7. Image Data Generator
8. MatplotLib

Steps for Execution:
1. To begin the project, I imported the dataset first and assigned variables to it using the os library. 
2. I further used ImageDataGeenerator module from tensorflow.keras.preprocessing.image so that we can rescale the training data images to 255 pixels so that the model should be      able to learn various features from the image for successfull classification.
3. Further identifying the categories of the images in the training data which were placed into the resprective folders, we extracted the images and named their categories based      on the names of their folders these being the categorical data.I also scaled he the images to a lower resolution i.e. to 64 px, 64 px but using an RGB image.
4. Further designed a neural network with first layer of 64 neurons and three hidden layers of 128 neurons each, followed by 2 Dense layers of 512 and one dense layer of 6 neurons    to classify the images into 6 categories.


* There were two activation functions used:
    1. for Hidden layers and Dense layers : 'ReLu'
    2. for Final Layer/ Output layer : 'softmax' for giving the output in 6 categories

* To compile the model we used 'Adam' as an optimizer, 'categorical_crossentropy' as Loss Function and metric used was 'Accuracy'.

5. The Model created was trained for 15 epochs which gave an Accuracy of around 87% reducing the Loss Function to 0.37.
6. Made some predictions with images downloaded from Google as well as the prediction set provided int he Dataset. The predictions displayed are accurate as per the response given    out by the model.
