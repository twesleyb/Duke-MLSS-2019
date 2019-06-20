# CNNs part 2.

Real CNN's will use more than 3 layers. Possibly 100s.

# 1D convolutions.
See an example of a convolution on [wikipedia](https://upload.wikimedia.org/wikipedia/commons/6/6a/Convolution_of_box_signal_with_itself2.gif)
* f the input feature image
* g the filter

Convolutional filters are feature detectors.
f is a feature from the image.
g was learned from the image.
What are the best filters to apply to an image to identify features that enable
you to classify the image correctly?

Think of passing a blurring filter over an image...

QUESTION: in many of the scientific applications of ML I can imagine, 
building a test training dataset is costly and may not be feasible 
at the scale required for ML. How to overcome?

Convolutional filters are feature detectors. 
Image + filter -convolution-> feature map

# Core elemetns of the CNN
* convolutional layers
	* filter size - shold be just large enough to capture small local features.
	* filter stride - decrease the size of the output for cp efficiency.
		downsample the input
	* filter (feature) number - the number of unique features. 
* activation function (think sigma function from MLP) - linear or non-linear fx
	* a weight... 
	* ReLU - non-linear activation function: rectified linear unit. 
	* This is similar to a real neuron! Output (APs) is all or none.
* pooling layers
* fully connected layers


Explore a neural network online (tf playground).

# Pooling layer.
Reduces computational complexity.
Combat overfitting

Max pooling. 
Applied to input. This may be though of as a part of the image normalization.
Less sensitive to absolute location in space = translational invariance

# Fully connected layer
input -Convolution-> -Pooling-> -Convolution-> Fully connected output
often there are multiple (latent) fully connected layers before final output.

# Gradient descent.
E the result of the empircal loss function.

Gradient descent is an optimization function. 
Stochastic gradient descent, performed in batches. 

# Summary
Convolutional neural networks recognize high level structure by building
heirarchical representations of image features.


