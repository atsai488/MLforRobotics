# Problem
Robots should meet two requirements.
1. Be capable at many tasks
2. Adapt to a new task quickly

Robots need large expert operated datasets that are fine tuned for the robot to use. It is unaccessible for regular humans to create these types of datasets by themselves. There is general coarse data that can be generated easily, however using that data to train a robot is harder as it is not nitpicked in a manner to help the robot on a specific task  

# Suggested Solution
1. Create a large dataset of training data.
2. Sift through the dataset to find training data that closely matches a video sample of the desired movement
3. Fine tune a model on the sifted data, where the base model is trained on the entire trained dataset

# Challenges
1. Allowing non-experts to create data - label the big dataset with a point tracking model and does the same with the hand
2. Sifting through data to match sub-trajectories to the filmed demonstration
3. Splitting up training data into sub trajectories

# Cool Ideas 
1. Splitting up sub-trajectories can be done as simple as splitting when the velocity goes below a certain threshold. Something simple can still be super effective
2. Knowledge to common things you work with in RL may not always be available/be the blocking factor from advancing. ie. Allowing robot state and action to be unknown can speed up other parts of data collection. 
3. Relative differences to match similarities instead of absolute position get rid of spatial awareness in sub-trajectories. Makes me think of translational invariance in CNN's. 

# Terms
1. DTW (Dynamic time warping) - comparing a two time series of speeds/lengths by minimizing the distance between the two. This is very similar to minimum number of edits to get the same string dynamic programming leet code problem.
2. LoRA (Low Rank Adaptation) - fine tune algorithm for LLMs, instead of trying to train the big matrix of weights, two smaller matrixes are trained which is much more efficient.

# Questions I have/Future works
1. In the process of labeling the gripper, a point tracking model was used. Does this mean that the camera position needs to be fixed?
2. Could the testing data be then reincorporated into the training data? One of the blockers I see is needing that large offline training dataset that the model was already trained on, defeating the purpose of adaptability in some sense.

#### Link
[link] https://arxiv.org/pdf/2505.20455 Labs: GLAMOR and Lira
