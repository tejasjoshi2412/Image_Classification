# Image_Classification

The project is based on the Intel Image Classification Dataset available of Kaggle. The Dataset includes the pictures of Buildings, Mountains, Glaciers, Street, Forest and Sea.
The file also contains results for the project.

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
6. Made some predictions with images downloaded from Google as well as the prediction set provided int he Dataset. The predictions displayed are accurate as per the response given out by the model.

**Results:

Accuracy and loss for Training Data:

Epoch 1/15
439/439 [==============================] - 150s 337ms/step - loss: 1.4991 - accuracy: 0.3630
Epoch 2/15
439/439 [==============================] - 154s 351ms/step - loss: 1.0182 - accuracy: 0.5883
Epoch 3/15
439/439 [==============================] - 157s 356ms/step - loss: 0.8943 - accuracy: 0.6439
Epoch 4/15
439/439 [==============================] - 159s 363ms/step - loss: 0.7840 - accuracy: 0.6988
Epoch 5/15
439/439 [==============================] - 160s 364ms/step - loss: 0.7099 - accuracy: 0.7408
Epoch 6/15
439/439 [==============================] - 161s 367ms/step - loss: 0.6224 - accuracy: 0.7792
Epoch 7/15
439/439 [==============================] - 159s 362ms/step - loss: 0.5947 - accuracy: 0.7854
Epoch 8/15
439/439 [==============================] - 159s 363ms/step - loss: 0.5464 - accuracy: 0.8069
Epoch 9/15
439/439 [==============================] - 160s 364ms/step - loss: 0.5092 - accuracy: 0.8162
Epoch 10/15
439/439 [==============================] - 160s 364ms/step - loss: 0.4994 - accuracy: 0.8232
Epoch 11/15
439/439 [==============================] - 160s 364ms/step - loss: 0.4371 - accuracy: 0.8420
Epoch 12/15
439/439 [==============================] - 160s 365ms/step - loss: 0.4224 - accuracy: 0.8502
Epoch 13/15
439/439 [==============================] - 159s 362ms/step - loss: 0.4120 - accuracy: 0.8569
Epoch 14/15
439/439 [==============================] - 159s 362ms/step - loss: 0.3845 - accuracy: 0.8668
Epoch 15/15
439/439 [==============================] - 158s 360ms/step - loss: 0.3700 - accuracy: 0.8665

Accuracy and Loss for the Test Data:

94/94 [==============================] - 7s 70ms/step - loss: 0.4910 - accuracy: 0.8340
Out[13]:
[0.49103549122810364, 0.8339999914169312]






