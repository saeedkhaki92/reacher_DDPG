# Report


## Actor Network


The actor network had three fully-conncetd layers. We used Batch Normalization in all layers except the output layer. The Relu activation function was used in all neurons except output layer which had tanh activation. The number of neurons in the hidden layers were 100, 100, and 4 (action size).


## Critic Network


The critic network had three fully-conncetd layers with respective 100, 100, and 1 neurons. The Relu activation function was used in all neurons except output layer which did not have activation function.

## Deep	Deterministic	Policy Gradient	(DDPG) Algorithm

DDPG is categorized as an Actor-Critic Approach in reinforcement learning litrature. It has two networks namely, actor and critic. Actor specifies action `a` given the current state of	the	environments. Critic value function	specifies	a	signal to criticize	the	actions	made by	the	actor.

Since DDPG uses deterministic	policy	gradient and it	might	not	explore	the	full state	and	action spaces, DDPG adds random noise to the actions to overcome this problem.

The critic is trained by minimizing the mean square error (MSE) between target Q values and local Q values like DQN method. The actor is trained by maximizing reward over a minibatch of samples. 


## DDPG Hyperparameter

- Batch size of 256 samples were used to trained the actor and critic.
- GAMMA of 0.99, which is the discount factor for the rewards.
- TAU of 0.001, which is the parameter for the soft update between target and local networks for both actor and critic.
- learning rate of 0.001 used to train the parameters of local networks for both actor and critic.
- weight decay of 0.0004, which was used for regularization.
- timesteps between updates was 20,
- starting epsilon of 1.0, which used for exploration of action and state spaces.
- fc1 number of neurons 100
- fc2 number of neurons 100
- Buffer size of 8e5, which holds past experinces like DQN approach. 

## Results


The environment solved in 146 episodes and the following figure shows the average score per episode.

![Alt Text](https://github.com/saeedkhaki92/reacher_DDPG/blob/master/result.png?raw=true)

## Discussion

One of the challenges in the projcet was to find the optimal network for both actor and the critic. I find two or there hidden layers with moderate number of neurons can solve the problem successfully. We also used batch normalization as recommended by the original DDGP paper. It can help with normalizing the input variables.

To improve the performance of DDGP, we used another small buffer (cache) to consider the most recent experience. It further improved the performance of the model. 

Using too many neurons in the actor or critic do not help since it cause overfitting.

### Future improvments
- Finding optimal network architecture for both actor and critic
- Finding optimal hyperparameters for DDGP algorithm such as buffer size and update schedule



