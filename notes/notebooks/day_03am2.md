# Learning!

A matrix of V words (number of words in vocabulary) by m (m-dimensions of 
semantic meaning of words).

y = U <dot> h + beta

Parameters to be learned: C, W, U, b, Beta (bias)

## How do we learn the models parameters?

p(Wout|Win;theta) | theta = model parameters C, W, U, b, Beta

We need some training data! 
Pairs of input and ouput:
Word<sub>in</sub> --> Word<sub>out</sub>

The possible combinations of words is too vast.
Use stochastic word descent to learn these relationships. 

Need access to data at scale: popularity of the iphone and advances in GPU.
Predicting the next word...

#### Using this approach we can build the geography of words!

# Recurrent neural networks
Sentances can have variable length.
Sentance of length N mapped to words Cm

Recurrence on hidden vector h...
Words are sequential data...

Word<sub>n-1</sub> --NN--> h<sub>n</sub> --> Sofmax pred: Next word
Word<sub>n</sub> --NN-->  h<sub>n+1</sub> --> Sofmax pred: Next word
Word<sub>n+1</sub> --NN-->  h<sub>n+2</sub> --> Sofmax pred: Next word

The meaning of each word in a sentance depends upon every other word.
However, it seems like the most important is the n-1 and n+1 words!

#### Goal of learning: learn relationships between input and output!

record a neurons input
record a neuron = output
ML learn relationship between input and output.
Predict output given some input

In the field of ML, empirical data have outpaced understanding!

What is h for the first word?! Zero?

This recurrent neural network is still not powerful enough to actually work!

Introduce memory cell, C.
In natural sentances, the preceeding word is often not enough to predict next word.

```
Baseball, that wonderful game dating back to the 14th century, involves running
around bases.
```
By the time you get to the word bases, h has nothing to do with baseballs.
H has exponential decay!
H forgets quickly.
Hence: long-term short-term memory

Utilize Tanh nonlinear function

Now four NNs!

Gating networks
o - output gate [0,1]
i - input gate [0,1]
f - forgeting gate

Memory Cells
c~<sub>n</sub>
the memory cell is updated with the partial memory of the previous memory cell
How does it know what to forget!?
Has a memory of ~1 sentance...

LSTM-Based text synthesis...



----
humans like stories, they aid our understanding.
but, stories introduce bias into the facts.  

----

