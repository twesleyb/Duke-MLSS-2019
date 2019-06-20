# Generative adversarial networks.
__Lecture by Ricardo Henao | Duke University__

## Sampling from discrete distributions, .e.g. a coin flip.
* p<sub>heads<\sub> = 0.5
* p<sub>tails<\sub> = 0.5
All outcomes are equally likely, also the roll of a die.

## Sampling from empirical distrubtions, e.g. pulling an object from a bag.
The probabily of seeing any object in the bag is its percent of the total.
Sampling with replacement.
We can draw at random from this distribution.

## The MNIST dataset.
Handwritting samples (N = 60,000 images)
We can sample from this distribution of images. 

## The ImageNet dataset.
Natural images (N > 1M images)
We can sample from this distribution as well.

## Sampling from a continuous distribution.
e.g. a distribution of 0's and 1's
There is an equal probability of drawing any number.
This is denoted as: `Uniform(0,1)`

__What if we have a distribution of data, but want to find data that is 
unlike this distribution?__

#### This is the problem that generative adversarial learning solves.

## Learning to sample from an unknown distribution.
[8] = f(epsilon)
* The handwritten digit 8, a complex object.
* The generator f, MLP or CNN.
* A simple object, epsilon.

## Autoencoding generative models.
Generation (forward): x = f(epsion; theta)
Learning (backward): Learn theta
```
Input -> Encoder -> Epsilon -> Generator -> Reconstruction - Input (loss)
```
Learn to minimize reconstruction error.
Goal: generate objects that look DIFFERENT from our known dataset!

Encode information into latent information (epsilon).
Problem: some samples do not look like digits!

The model is good at extracting features from the image and generating new images,
but it does not know how to make them look like real digits!

## Learning adversaarially.
What if we had an expert judging the quality of the generated samples?
Like a wine critic judging the synthesized wines.
The generated wine looks the same! 
But, does it taste the same?

Output from the model x is compared to the real image by the critic in order to 
determine the probability that x is real.

## Generative adversarial networks (GANS)
1. Learn theta (generator): we want to make good digits.
	* minimize the ability of the critic to tell the difference between
	  real and fake.
2. Learn psi (critic): we want the critic to be good.
	* maximize the ability of the critic to detect fakes. 
3. Repeat: both the generator and critic improve!
4. Stop once both stop improving (equilibrium is reached).

## Learning adversarially.


