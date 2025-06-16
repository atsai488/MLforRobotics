These are lists of questions that I have and often ask myself. I want to answer them so I can try to ingrain them in my head.

1. Why does log randomly appear in so many equations?
- "Log derivative trick", allows us to move the gradient inside the expectation which is essential for estimating gradients
- The gradient of the expected value of a function of x, where x is sampled from the distribution p is equal to the expected value of the function multiplied by the gradient of the log of distribution p.

2. What is the different between p and pi in equations? Aren't they both probabilistic distributions that we are sampling from?
- pi is the policy of the agent. It takes in a state and outputs either a probability distribution of actions or an action.
- p is the probability notation. For the specific question that made me write this question. It was "p subscript theta of x". Well it really depends on what X is. If X was a trajectory, it would the probability of that trajectory occurring given theta, the parameters of the policy. This includes the probability of being in the initial state and taking all those actions in that order.