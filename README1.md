# Hand Writing Recognition Using Convolutional Neural Networks

The MNIST problem is a dataset developed by Yann LeCun, Corinna Cortes and Christopher Burges for evaluating machine learning models on the handwritten digit classiﬁcation problem. The dataset was constructed from a number of scanned document datasets available from the National Institute of Standards and Technology (NIST). 

 Each image is a 28×28 pixel square (784 pixels total). A standard split of the dataset is used to evaluate and compare models, where 60,000 images are used to train a model and a separate set of 10,000 images are used to test it. It is a digit recognition task. As such there are 10 digits (0 to 9) or 10 classes to predict. Results are reported using prediction error, which is nothing more than the inverted classiﬁcation accuracy. Excellent results achieve a prediction error of less than 1%. State-of-the-art prediction error of approximately 0.2% can be achieved with large Convolutional Neural Networks. 


# Requirements
  -  Python 2.7
    -  Tensorflow
    -  Keras
    -  numpy
    - matplotlib
    - pandas
    - jupyter notebook

# Dataset
 - The model is trained on the MNIST dataset downloaded from Kaggle.

# Model

 ![CNN MODEL](https://github.com/Ashwini-Analytics/Python_DataAnalysis_Code/blob/master/Handwritting_digit_recog_CNN.jpg)
 
 - The ﬁrst hidden layer is a convolutional layer called a Conv2D. The layer has 32 feature maps, with the size of 5×5 and a rectiﬁer activation function. This is the input layer, expecting images with the structure outline above.
 
 - Next we deﬁne a pooling layer that takes the maximum value called MaxPooling2D. It is conﬁgured with a pool size of 2×2.
 
 - The next layer is a regularization layer using dropout called Dropout. It is conﬁgured to randomly exclude 20% of neurons in the layer in order to reduce overﬁtting.

 - Next is a layer that converts the 2D matrix data to a vector called Flatten. It allows the output to be processed by standard fully connected layers.
 
 - Next a fully connected layer with 128 neurons and rectiﬁer activation function is used.
 
 - Finally, the output layer has 10 neurons for the 10 classes and a softmax activation function to output probability-like predictions for each class.


