# Chapter 2.1: Mathematical Foundations of Reinforcement Learning

This chapter delves into the core mathematical concepts that form the bedrock of Reinforcement Learning. Understanding these principles is crucial for designing and implementing effective intelligent agents.

## Key Concepts

### Markov Decision Processes (MDPs)
A Markov Decision Process is a mathematical framework for modeling decision-making in situations where outcomes are partly random and partly under the control of a decision-maker. An MDP is defined by:
- A set of states (S)
- A set of actions (A)
- A transition probability function P(s'|s, a)
- A reward function R(s, a, s')
- A discount factor (γ)

### The Bellman Equation
The Bellman equation is a fundamental concept in RL that expresses the relationship between the value of a state and the values of its successor states.

For a given policy π, the value of a state `s` is given by:
`Vπ(s) = E[Rt+1 + γVπ(St+1) | St=s]`

The optimal value function `V*(s)` is defined by the Bellman optimality equation:
`V*(s) = max_a E[Rt+1 + γV*(St+1) | St=s, At=a]`

This can be rewritten as:
`V*(s) = max_a Σ_{s'} P(s'|s, a) [R(s, a, s') + γV*(s')]`

### Value Iteration and Policy Iteration
- **Value Iteration**: An algorithm that iteratively updates the value function until it converges to the optimal value function.
- **Policy Iteration**: An algorithm that alternates between policy evaluation and policy improvement to find the optimal policy.

These concepts are the building blocks for many RL algorithms, from Q-learning to modern Deep RL methods. A solid grasp of this math is essential for the chapters that follow.
