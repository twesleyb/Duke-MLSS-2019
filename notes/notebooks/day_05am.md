# Reinforcement Learning
__Lecture by Lawrence Carin__

How do we get enough data to do ML?
Reinforcement learning may help us do this.

A machine beats a human GO player.
How can you teach a machine to play GO?
Reinforcement learning!

Reinforcment learning attempts to achieve the best outcome in the most 
cost effective manner. Like human systems, it uses trial and error to 
learn a policy--the optimal way for a system to operate.

* Positive outcomes are reinforced.
* Negative outcomes are not rewarded.

## Semantics of reinforcement learning.

#### Patients state (s):
Set of observations that define the patients state are represented by the
vector s.

#### Doctors actions (a):
Set of potential actions that may be taken are defined as A = {a1,a2,...}

#### Stochastic response to action a.
There is some randomness in how a patient's state s will respond to action a.

__Markovian Probability:__
Let P(s,a,s') represent the probability that when a patient in state s will 
move to state s' in response to action a.
    Probability( s -a-> s' )

#### Reward (r) of taking action a and changing patients state.
Let r(s,a,s') represent the net reward associated with taking action a and 
transition from s -> s'.

The reward r reflects both the cost and benifit of taking action a.

#### Learning is the sequential process of state -> action -> reward.
The learned policy is the set of actions that maximize average reward.
This policy should take into account the long term impact of action ai.
That is, the policy should not be myopic.

## Problem.
We typically do not know P(s,a,s')
How can we learn the policy without this?
We can use trial and error!

__Reinforcment learning is the formalization of this challenge!__

## Simple, intuitive solution.
Assume the patients state s is defined by the minimum and maximum blood glucose
concentration on the previous day. 
* Discretize the continous range of state values into n bins.

The action a may be the rate of continous insulin supply and the bolus dose.
* Discretize the continous range of action values into m bins.

## Q Learning
The function Q(s,a) is an nxm matrix denoting the value of taking action 
a in state s. We want to learn the function Q, so we can predict the outcome
of any given action for any given state!

Q<sub>old<\sub> is the prior/old value for the Q function when we take action a.

#### Temporal difference (TD):
Update Q: if reward is larger than expected, then the probability of taking 
this action is increased! If reward is smaller than expected, then the 
probability of taking this action is decreased! And we continue...

The learning rate is defined as alpha ($\alpha a$).

__PROBLEM: This strategy is myopic! How do we fix this.__

## Extension to fix the problem.
Modify the temporal difference (TD):
r(s,a,s') + $\gamma g$ * max(Qold(s',a'))
Gamma is the discount factor between 0 and 1. 
This term accounts for an individuals bias towards imediate or long term reward.

> "In the long run we are all dead."
>     _John Maynard Keynes | A Tract on Monetary Reform (1923)_

## Balancing exploitation and exploration.
Exploration is necessary to learn new solutions!

## $\epsilon e$-Greedy: Exploration and Exploitation
How likely are we to choose an unusual action?
We choose epsilon.


