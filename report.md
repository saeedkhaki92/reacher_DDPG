# Report


## Actor Network


The actor network had three fully-conncetd layers. We used Batch Normalization in all layers except the output layer. The Relu activation function was used in all neurons except output layer which had tanh activation. The number of neurons in the hidden layers were 100, 100, and 4 (action size).


## Critic Network


The critic network had three fully-conncetd layers with respective 100, 100, and 1 neurons. The Relu activation function was used in all neurons except output layer which did not have activation function.

## DDPG Hyperparameter

- Batch size of 200
- GAMMA of 0.99
- TAU of 0.001
- learning rate of 0.001
- weight decay of 0.0004
- times between updates 100
- starting epsilon 1.0
- fc1 number of neurons 100
- fc2 number of neurons 100




