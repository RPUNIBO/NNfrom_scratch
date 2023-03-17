# NNfrom_scratch
we develop a Neural Network from scratch, just using mathematical libraries of numpy.

Then we define a couple of activation functions (sigmoid and relu) and their derivatives.

A neural network is just a collection of numerical vectors describing the weigths of the links at each layer. For instance, a dense layer between n input neurons and m output neurons is defined by a matrix w of dimension nxm for the weights and a vector b of dimension m for the biases.

Supposing the network is dense, its architecture is fullly specified by the number of neurons at each layer. For our example, we define a shallow network with 8 input neurons, 3 hidden neurons, and 8 output neurons, hence with dimension [8,3,8].

We initialize weights and biases with random values.

For the backpropagation algorithm we also need to compute, at each layer, the weighted sum z (inputs to activation), the activation a, and the partial derivative d of the error relative to z.

We define a version of the backpropagation algorithm working "on line", processing a single training sample (x,y) at a time, and updating the nework parameters at each iteration. The backpropagation function also return the current error relative to (x,y).

An epoch, is a full pass of the error update on all training data; it returns the cumulative error on all data.

Then we define same data and fit the network over them.

We want to define a simple example of autoencoder, taking in input a one-hot representation of the numbers between 0 and 7, and trying to compress them to a boolean internal representation on 3 bits.

