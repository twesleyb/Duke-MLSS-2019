# Gernalization Error in neural networks
__Lecture by Henry D. Pfister | Duke University__

## Deep Neural networks (DNNs)
Recent performance of DNNs has lead to surge in popularity. This resurgance
has prompted several important theoretical questions:
* With more parameters than data, why do DNN's generalize?
* With zero training error why don't they overfit?

Recent advances in our understanding:
over parameterization -> optimization without overfitting!
large NNs have loss landscapes with connected minima
themes: stochastic gradient descent, flat minima, kernel methods

More work needed to bring together multiple partial explainations!

## Setup
(x,y) for classification into d classes use one-hot 
Use cross entropy loss

## Training
Loss landscape -- adjust theta to minimize loss
We can utilize:
Our entire dataset = full-batch
subset of our dataset = mini-batch
* Gradient descent
* Stochastic gradient descent - random mini-batches
Generalization = minimize theta without knowing test data!

## Questions?
Will GD reach a local or global minima?
What is the error rate on the training data? the test data?
How does network complexity effect performance?
What is the effect of overparametrization?

## Answers
Gradient descent can reach global min with zero error
Stochastic gradient descent may be biased towards flat minima
Performance only weakly depends on parameters and optmization method

## The bias-variance trade-off
An overly simple model cannot account for the complexity of the data.
An overly complex model will overfit the data = not generalizable

An overly complex model may produce small training error, but may not
be generalizable and therefore have increased testing error.

Overfit = too many training epochs.

## Rethinking generalization in DNNs.
Regularization: penalize complex models.
small minibatch = 256
large minibatch = 5,000

optimizers: SGD and ADAM

## Vizualizing the loss landscape.
Why are deep (more layers) neural networks better?

## The classic bias-variance trade-off is almost right.




