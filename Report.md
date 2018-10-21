# Summary

Implmented a vanilla DQN and benchmarked against Double DQN, Duelling DQN and both Double and Douelling DQN. The benchmark was the number of episodes to reach a moving avreage of at least 15.0 over 100 episodes.

The network is a three layer fully connected layers (200, 100 and 50) with RELU activations. When using duelling two additinonal fully connected layers are added for the Value and Advantage values.

[DQN](https://arxiv.org/abs/1312.5602) <br>
[Double DQN](https://arxiv.org/abs/1509.06461) <br>
[Duelling DQN](https://arxiv.org/abs/1511.06581) <br>

## Episodes to reach target of 15.0
**Vanilla DQN:** 697 episodes <br>
**Double DQN:** 602 episodes  <br> 
**Duelling DQN:** 499 episodes  <br>
**Duelling and Double DQN:** 537 episodes  <br>


## Discussion
Duelling DQN performs better alone than together with Double DQN. Not sure why. My experiment was limited to one run per configruation so it is not statistically significant. Random initialization of weights and random chosing of actions early in exploring can affect the outcome greatly. More runs are needed to determine Duelling DQN alone is better than both Double and Duelling DQN.
