# RLQ-learningTradingAI
Reinforcement Learning briefly is a paradigm of Learning Process in which a learning agent learns, overtime, to behave optimally in a certain environment by interacting continuously in the environment. The agent during its course of learning experience various different situations in the environment it is in. These are called states. The agent while being in that state may choose from a set of allowable actions which may fetch different rewards(or penalties). The learning agent overtime learns to maximize these rewards so as to behave optimally at any given state it is in. Q-Learning is a basic form of Reinforcement Learning which uses Q-values (also called action values) to iteratively improve the behavior of the learning agent.

Q-Values or Action-Values: Q-values are defined for states and actions. Q(S, A)  is an estimation of how good is it to take the action A  at the state S  . This estimation of Q(S, A)  will be iteratively computed using the TD- Update rule which we will see in the upcoming sections.
Rewards and Episodes: An agent over the course of its lifetime starts from a start state, makes a number of transitions from its current state to a next state based on its choice of action and also the environment the agent is interacting in. At every step of transition, the agent from a state takes an action, observes a reward from the environment, and then transits to another state. If at any point of time the agent ends up in one of the terminating states that means there are no further transition possible. This is said to be the completion of an episode.
Temporal Difference or TD-Update: The Temporal Difference or TD-Update rule can be represented as follows :This update rule to estimate the value of Q is applied at every time step of the agents interaction with the environment. The terms used are explained below. :
S  : Current State of the agent.
A  : Current Action Picked according to some policy.
S'  : Next State where the agent ends up.
A'  : Next best action to be picked using current Q-value estimation, i.e. pick the action with the maximum Q-value in the next state.
R  : Current Reward observed from the environment in Response of current action.
$\gamma$  (>0 and <=1) : Discounting Factor for Future Rewards. Future rewards are less valuable than current rewards so they must be discounted. Since Q-value is an estimation of expected rewards from a state, discounting rule applies here as well.
$\alpha$  : Step length taken to update the estimation of Q(S, A).
Choosing the Action to take using 
*** QuickLaTeX cannot compile formula:
 

*** Error message:
Error: Nothing to show, formula is empty
-greedy policy: $\epsilon$  -greedy policy of is a very simple policy of choosing actions using the current Q-value estimations. It goes as follows :

With probability (1-$\epsilon$)  choose the action which has the highest Q-value.
With probability ($\epsilon$)  choose any action at random.
Pros: 

Long-term outcomes, which are exceedingly challenging to accomplish, are best achieved with this strategy.
This learning paradigm closely resembles how people learn. Consequently, it is almost ideal.
The model has the ability to fix mistakes made during training.
Once a model has fixed a mistake, there is virtually little probability that it will happen again.
It can produce the ideal model to address a certain issue.

