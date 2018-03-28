# LeNet-5 Architecture
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

![LeNet-5 Architecture](images/lenet.png)
Implementation of the LeNet-5 deep neural network model for the [MNIST](https://en.wikipedia.org/wiki/MNIST_database) dataset using tensorflow.

The code can be found in the [LeNet jupyter notebook](LeNet.ipynb).

## Input
The LeNet architecture accepts a 32x32xC image as input, where C is the number of color channels. Since MNIST images are grayscale, C is 1 in this case.

## Model Architecture
**Layer 1:** Input is 32x32x1.

* **Convolutional** with 5x5x6 Filter, output shape is 28x28x6.

* A **Relu** activation function is applied.

* A **max pooling** 2x2 with a stride of 2 is the output of the first layer (shape 14x14x6).

**Layer 2:** Input is 14x14x6.

* **Convolutional** with 5x5x16 Filter, output shape is 10x10x16.

* A **Relu** activation function is applied.

* A **max pooling** 2x2 with a stride of 2 is the output of the second layer (shape 5x5x16).

* **Flatten.** the output (400).

**Layer 3:**

* **Fully Connected.** (400, 120)
* A **Relu** activation function is applied.

**Layer 4:**

* **Fully Connected.** (120, 84)
* A **Relu** activation function is applied.

**Layer 5:**

* **Fully Connected (Logits).** (84, 10)

