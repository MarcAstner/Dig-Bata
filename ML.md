Week 5: Machine learning


ML_gym_reinforcment:

The neureal network consists of two dense layers using the same activation of relu, it was choosen for his simple calculability wich works very well with a small amount of parameters.
The output was given in the third dense layer, sized two the amount of possible actions. The inital parameters for training were changed.

parameters:
MAXRUNS = 50
GAMMA = 0.975 - needs to be high enough to be significant
LEARNING_RATE = 0.00125 - too high=fast learning in the beginning and very slow later on, vice versa
MEMORY_SIZE = 100000 - important in combination with batch size and learning rate
BATCH_SIZE = 32 - if too big=slower computations

optimizer adam proved to be very compatible with linear activations such as relu in this exercise


cilfar cnn:
This neural network consists of convolutional and pooling layers. These are mandatory for an image processing NN. Simple models showed high accuracy(85%+) during training and very low accuracy(65%)during testing.
This is a clear sign for overfitting. In order to counteract this I tried implementing Batch_Normaliztion layers as well as kernel_regularizers to regulate the weight they place on the neurons.
Including these options the model showed a better validation accuracy of (75%). Though it took way more epochs.
Initally I even underfitted the training because I implemented to many restricting factors/layers like multiple dropout function.
The amount of parameters was also important, best results were generated with roughly 3-4 million parameters, resulting in longer computation time.

edit: I tried using multiple different activation functions together, though this has proven futile. The best results were gathered by sticking with one activation function. Even adding similar add on functions like Leaky Relu and Prelu that should help with backwards computability of the parameters were not that promising, though I had only limited time testing them and there is a good chance that they are benefical in larger, more complicated models.




note: the code in my github for the cilfar cnn was corrupted so i needed to rerun it last minute. Due to a lack of time I needed to stop the code and use the old confusion matrix. The underfit file was the only file i had computed.
edit: It is finshed running with the correct code, the parameters were changed so the amount of parameters was less aswell as the computation time. I am sorry that I uploaded the correct file ML_cilfar_CNN_bestfit.ipynb 30 minutes late but i just moved back home today due to boarder closing. 
