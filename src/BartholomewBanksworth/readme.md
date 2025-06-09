# Overview of this project

An RL model that plays monopoly against you! This was my first exposure to coding a reinforcement learning model. We used OpenAI's gym library with the simplification of using SIMPLE. Another library that made it easier to interface with OpenAI's gym. The process of coding this project taught me the basics of RL.

## Takeaways
Action spaces, observation spaces, creating an environment, discrete vs. continuous actions, and reward function. This was definitely an ambitious first project but it was a great "go at it" type of project. Definitely struggled at first with wrapping my head around the concepts and figuring out what things meant. Eventually, while working in a team, we were able to get a running program which was amazing.

A short coming of this project is definitely the reward function and training of the model. Our naive reward function is based on the property value and current money that you have. It is an extremely biased reward function that priorities spending for ownership of property. I believe this is a largest inductive bias that we have coded for our model. I did not let the model explore for strategies by itself. I knew this while I was coding up the reward function, however, we did not have the compute power or time to fix it as this was a project I did for a school club and we finished it at 3 AM the day of the showcase :). 

## Conclusion
This definitely was the start of my journey with RL, and it is patchy work at best. I do think it was an amazing introduction though, abstracting away the less relevant parts of ML like the optimization algorithms, and just giving me a basic introduction to what an environment is.