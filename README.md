# Reacher Project 


 In this project, I used Deep Deterministic Policy Gradient algorithm (DDPG) to solve the Reacher environment.

## Environment

This project uses the reacher environment from Unity environment provided by Udacity team.

- State space is continous with size of `33`.

- Action space is continous with size of `4`, each in the interval of `[-1,1]`.

- The environment gives a rewards of between `[0, 1]` for reacher that correctly position the hand. 

The environmnet is considered to be solved if the average score is above `30.0` over last `100` episodes.

![Alt Text](https://raw.githubusercontent.com/Unity-Technologies/ml-agents/master/docs/images/reacher.png)


## Getting Started

- Clone the <a href="https://github.com/udacity/deep-reinforcement-learning" target="_blank">udacity deep reinforcement learning repository</a>

- Follow instructions there to install the depndencies. List of all used packages can be found in the `requirment.txt`.


- <a href="https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control" target="_blank">Download</a> the unity environment which matches your operating system 


- Run the jupyter notebook.

## Checkpoints

The saves folder provides the trained weights for both actor and critic in Pytorch format.

## References and Credit

The most of the codes were originally provided by Udacity team and other online open source websites. 




















