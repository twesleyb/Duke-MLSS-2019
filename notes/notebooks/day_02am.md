# Deep convolution of neural nets (part 1).
__Lecture by Tim Dunn__
Tim is from Eva Naumann's lab in neurobiology.

Very common ML application for image analysis. 

Application: analysis of health and unhealthy retina for the 
diagnosis of diabetic retinopathies. This works very well.

Gulshan et al., 2016 | JAMA
Evaluate performance of algorith by plotting:
_Sensitivity versus 1-specificity_

Sensitivity = number of true positives / total number of positives
Specificity = number of true negatives / total number of negatives

Also used by the TSA for screening. Identification and classification of 
prohibited items. 

Markerless motion capture: DensePose (Facebook)
Markerless motion capture: analysis of animal behavior (Mathis et al., Nat. 
Neuro. 2018)

Style transfer and harmonization (Gatys et al., arXiv 2015)

# Convolution neural networks find structure in images.
Consider a simiple example of classification of a written digit by a 
multilayer perceptron (MLP). 

_Problem_: what if location of 2 has been moved from center of image?
The MLP will fail!

CNN can achieve translational invariance by applying a repeated transformation
across the entire image.

# CNN's take advantage of repeated, heirarchical structure in images.
This structure is __naturally__ present in images!

Repeated - simple elements that are repeated throughout an image.
* Vertical lines, horizontal lines
Heirarchical - these elements make up mid-level structures, geometric shapes. 
* high level structure - composition of shapes that make a bear or a train.

CNN's undo this heirarchy. low -> mid -> high

# CNN's apply a convolutional filter to an image.
Different filters for different low-level elements of an image.

How do CNN's achieve scale invariance?
How do CNN's or the user pick filters?

The output of a convolutional filter applied to an image is a feature map.
This is a heatmap of a low level element in a n image.

Low-level feature map
Mid-level filters to identify compositions of low-level elements. 

Iterative application of convolutional filter to identify low, mid, and high 
level features in an image.

There is a massive number of combinations of low level elements. How to 
decide which combinations of low level features are meaningful?
The network learns these filters...

The filters that the network arrive at are often re-used (e.g. edge detection).
But, in practice it is best to have the MLA learn them. If dataset is limited,
then filters may be chosen in advance.

# How do we define the models parameters?
input image In
* layer 1 filters sigma1 ... phik (k number of filters)
* layer 2 filters phi1 ... phik (k does not need to be equal)
* layer 3 filters omega1 ... omegak
* This is passed to a MLP. 
Parameters at each step are "learnable"

# Cost function versus model parameters.

# The CNN approach is analgous to how the human brain and regina process images!

# Transfer learning.
What to do if input number of images is not so large (100,000).

Preinitialization to speed up training and improve performance.
Training on a larger dataset to learn the weights.

* Transfer learning exploits the fact that low-level detectors detect common
elements in all images. 

We learn the parameters by minimizing loss. 
