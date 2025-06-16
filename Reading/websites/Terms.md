I started this list as a way to remember specific to RL jargon. Some of these terms are going to be basic and I defined them the way I interpret them; others I genuinely had no idea what they meant until I searched it up online and read a short article.

## Vanilla RL
1. Value function - the measure of how good being in a state is
2. Policy - the "brain" of how an agent will operate in an environment. The policy takes in the state observation as an input and outputs an action to take
3. Q-function - The quality of being in a state and taking an action. This is really powerful as the bellman optimization equation allows us to implicitly define a Q-function. This means we don't need to necessarily know the model of the environment. If we optimize for our current s and a, then eventually it will work out.
4. model vs model - Less of a term but just confusion. Model free means you do not use the rules of the environment/know the rules and train an agent while on model means you use the specific rules of the environment to train your agent. The other meaning for Model is the RL model, but I often like to refer to it as agent instead because I think that word encapsulates the idea of what it does better. This could be completely wrong, but this is my list :)
5. Advantage Function - Difference between the Q-value for a state action pair and the value function.

## Error related terms
6. Temporal Difference Error - formally defined as *(Current Reward + discount factor x Value of next state) - Value of current state*, It is a good estimator for the advantage function since the first term of the equation is just the Quality function.


### Non RL-specific terms but just English
1. Temporal - Usually dealing with time
2. heuristics - learning through trial and error, very laissez faire learning so to speak.
3. 