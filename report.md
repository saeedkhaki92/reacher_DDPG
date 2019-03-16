# Report


## Actor Network


The actor network had three fully-conncetd layers. We used Batch Normalization in all layers except the output layer. The Relu activation function was used in all neurons except output layer which had tanh activation. The number of neurons in the hidden layers were 100, 100, and 4 (action size).


## Critic Network


The critic network had three fully-conncetd layers with respective 100, 100, and 1 neurons. The Relu activation function was used in all neurons except output layer which did not have activation function.

## DDPG Hyperparameter

- Batch size of 256
- GAMMA of 0.99
- TAU of 0.001
- learning rate of 0.001
- weight decay of 0.0004
- times between updates 100
- starting epsilon 1.0
- fc1 number of neurons 100
- fc2 number of neurons 100
- Buffer size of 8e5

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



