# TLDR
Simplest form of optimization. It uses Calculus 3 to calculate the gradient in a high dimensional space to maximize the expected reward.

# My words
This one is closely related to general ML, the only difference is that you need to collect the data instead of having it already preprocessed. You still do the same gradient ascent gymnastics using optimizers like adam and then reduce the error between the observed value function and current value function by doing gradient descent. This algorithm is *on Policy* which means it will always choose the option base on the most recent iteration of the policy. It makes it more stable but will get trapped in local maxima as it will do the same thing instead of exploring new avenues and finding something better.

#