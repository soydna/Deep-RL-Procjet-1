# Report

Implmented a vanilla DQN and benchmarked against Double DQN, Duelling DQN and both Double and Douelling DQN. The benchmark was the number of episodes to reach a moving avreage of at least 15.0 over 100 episodes.

[DQN](https://arxiv.org/abs/1312.5602) <br>
[Double DQN](https://arxiv.org/abs/1509.06461) <br>
[Duelling DQN](https://arxiv.org/abs/1511.06581) <br>


## Architecture
The network is a three layer fully connected layers (200, 100 and 50) with RELU activations. When using duelling two additinonal fully connected layers are added for the Value and Advantage values. The non duelling verions instead has an output layer.


## Hyperparameters
BUFFER_SIZE = int(1e5)  # replay buffer size <br>
BATCH_SIZE = 64         # minibatch size <br>
GAMMA = 0.99            # discount factor <br>
TAU = 1e-3              # for soft update of target parameters <br>
LR = 5e-4               # learning rate  <br>
UPDATE_EVERY = 4        # how often to update the network <br>


## Episodes to reach target of 15.0
**Vanilla DQN:** 697 episodes <br>
**Double DQN:** 602 episodes  <br> 
**Duelling DQN:** 499 episodes  <br>
**Duelling and Double DQN:** 537 episodes  <br>


## Discussion
Duelling DQN performs better alone than together with Double DQN. Not sure why. My experiment was limited to one run per configruation so it is not statistically significant. Random initialization of weights and random chosing of actions early in exploring can affect the outcome greatly. More runs are needed to determine Duelling DQN alone is better than both Double and Duelling DQN.

## Future Work
* Run the experiment several times to verify Duelling DQN alone is better than Both Duelling and Double DQN
* Implement all Rainbow enhancements and run experiments to verify performance. [Rainbow](https://arxiv.org/abs/1710.02298)
