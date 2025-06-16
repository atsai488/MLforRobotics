# Problem
Teaching robots new behaviors need a specific, expert example for each new scenario. This is time consuming and is not sample efficient. Using RL, you can use reward functions as the "Teacher" but they are equally hard to design and create.

# Suggested Solution
1. train a language reward model on the few demonstrations (Reward function training)
2. train a language conditioned policy with data collected offline (Policy training)
3. Fine tune with new trajectories via ONLINE rl
4. Solve SIMILAR tasks to the original demo

# Challenges
1. Limited data: the more I read about what is going on at the forefront of RL, the more I realize its about using data efficiently. Sure there are sometimes ground breaking methods for training/optimization algorithms, however, most progress is done by using existing methods in a clever manner to create something new. 

# Cool Ideas 
1. Augmenting data.
    - The small number of demonstrations causes the RL policy to overfit to the specific points. It is hard for it to learn a general policy because it has little data to work with. By creating fake "bad" trajectories/demos, the data set can grow larger without needing additional demonstration/time from a human.
    - Creating more instructions by prompting LLMs
2. Being smart with labeled information
    - Positional embeddings are useful to tell time, however, by adding too many positional embeddings, the model can cheat by saying oh "if something lasted this long, it should be a success learn from it" at least that sort of idea.

# Terms
1. language-conditioned reward model - using natural language to represent a reward function, often times this means using a Large Language Model, but this paper uses a task description and execution video as the "ground truth"
2. offline rl vs online rl - Offline means using already collected data, Online means interacting with the environment.
3. DINOv2: image encoder that is commonly used (strong object-centric representations)
4. IQL, implicit quality function learning
# Takeaway
What I wrote in challenges is one thing I am starting to realize. It is necessary to also focus on the bigger picture. As scientists, we get rabbit-holed into our work and forget what practical use cases we can have with our projects. It is great if there is a robot with a policy allowing it to do a backflip, however, it loses a lot of value when it becomes unaccessible to a regular human because of the training cost. Quick and easy use is of equal importance.

Using light weight models/embeddings can help speed up the process of training. Combining language and image embeddings can be done by using cross-modal sequential aggregators. 

# Questions I have/Future works
1. Implicit Q-Learning and how it works. A concept I do not understand. 
2. The current method to offer dense feed back through limited data is by creating fake data. Are there optimization algorithms that could better take advantage of more information being leaked out of human demonstrations instead? Giving the demos a richer meaning.
#### Link
[link](https://arxiv.org/pdf/2505.10911) Labs: GLAMOR, Lira, and Amazon
