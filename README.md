# MNIST & LeNet-5
## What Is MNIST and Goal For This Project
* The MNIST dataset is a large database of handwritten digits that is commonly used for training various image processing systems. It contains 60,000 images of training set and 10,000 images of test set. The handwritten digit images have been size-normalized and centered in a fixed size of 28×28 pixels. 
* I used a slightly modified LeNet-5 model to train these images and resized the images to 32x32 pixels beforehand.
<div align="center"><img src="pictures/mnist_data.jpg" width="400" alt="Material Bread logo"></div>
<p align="center"> MNIST Dataset </p>

## LeNet-5 Architecture
<div align="center"><img src="pictures/lenet-5.jpg" width="700"></div>
<p align="center">LeNet-5 Original Architecture</p>  
<p></p>
LeNet-5 is a very efficient convolutional neural network for handwritten character recognition. It is a small network that has 7 layers and contains basic modules of deep learning: convolutional layer, pooling layer and fully connected layer. Moreover, LeNet-5 uses average pooling and tanh activation function. However, in this project I will use max-pooling and ReLU activation function. The rest of the configurations are the similar to base architecture.

<h2 align="center">LeNet-5 Parameters</h1>
<div align="center"><img src="pictures/lenet_layer.jpg" width="500"></div>

### How to calculate parameters for each layer
Recall that there are no trainable parameters in max-pooling layers and ReLU activation functions
* Conv2d (2-1):  ((5x5x1)+1)  x 6 = 156
* Conv2d (2-4):  ((5x5x6)+1)  x 16 = 2416
* Conv2d (2-7):  ((5x5x16)+1) x 120 = 48120
* Linear (2-10): (120+1)      x 84 = 10164
* Linear (2-12): (84+1)       x 10 = 850
 
### Graph
<p align="center" width="100%">
    <img width="32%" img src="pictures/graph1.png", height = 350, width = "350"> 
    <img width="32%" img src="pictures/graph2.png", height = 350, width = "350"> 
</p>
