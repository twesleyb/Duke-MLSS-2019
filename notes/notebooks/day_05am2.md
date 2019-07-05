# Reinforcment learning part 2.
__Lecture by Lawrence Carin__

## Q-Learning.
The most populuar method of reinforcement learning.

__Limitations:__
* The Q function is a matrix of states/actions. This large look-up table 
  becomes impractical when there are a large number of states.

Represent Q-function as a neural network.
Redefine state as a continuous vector...

Deep convolutional neural network- ML's main tool.
Overcoming the problem of needing a lot of data for ML.

Humans can recognize an object that looks unlike any example of that object
that they have seen before! Maybe ML can do the same thing.

## Deep Q Learning (DQN)
$/pi p$(s) = argmax(Q(s, a, $/theta t$))

Learning the CNN's parameters theta. 
Update the models parameters instead of large look up table.
The neural network is a function, Q. 

The table was the state->action pairs.
This table is replaced by the neural network.
CNN [ state --> --> action ] 

The output of the Q-learning CNN is a Qvalue- the quality of the action.

Recurrent neural networks -- predict the next thing. No reward term.

Q-learning is ML-cost benefit analysis. Iterative. 

Major fields of ML
MLP - multilayer perceptron
CNN - convolutional neural networks
RL - reinforcment learning

## Gradient descent
Learning the minima of a function.

Other methods:
Bayesian

