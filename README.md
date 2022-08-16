# PClub Secy Recruitment Task - 4
## Aniket Suhas Borkar - 210135
  
This repository contains the Jupyter notebook containing the code I wrote to implement a neural net with a single hidden layer, from scratch.  
  
Colab link - 

The neural net implemented serves the purpose of digit recognition. It has been trained and subsequently tested using the MNIST database of handwritten digits. The major features of the neural net include:  
- The input of the neural network are the brightness values of the individual pixels of an image, for which the digit is to be recognised. The net accepts 28X28 pixel images as input.
- The net has a single hidden layer with 20 neurons in it.
- The net outputs the prediction to the output layer containing 10 output neurons.
- The net uses the logistic sigmoid function as the activation function for the hidden and output layer neurons.  
  
  
The net has been trained using the training set of the MNIST database containing 60000 labelled samples. The test set of the MNIST database has 10000 labelled samples.  
  
In order to train the model, backpropagation and stochastic gradient descent have been used. I first randomly shuffled the training set, and then chose sets of 10 samples from the (shuffled) training set and fed it to the net to calculate the outputs. Then, taking a quadratic cost function, I calculated the average cost for this set of 10 samples. The aim is to minimise this cost. So using backpropagation, the gradient is calculated, and the weights are updated by using this gradient. A learning rate has been defined which is used to decide how fast the weights and biases are updated (it is used to scale the gradient before subtracting the gradient from the weights' matrix). This process was repeated till all the samples in the training set were used. To make the net learn effectively, this process was repeated multiple times each time decreasing the learning rate. I trained the net with 30 iterations over the training set for learning rates - 2.0, 0.4, and 5 iterations with a rate of 0.01.  
  
The model achieves an accuracy of 60.34%.
