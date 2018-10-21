# The Environment
*Copied from Udacity Project description*

In this project an agent will be trained to navigate (and collect bananas!) in a large, square world.


A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around the agent's forward direction. Given this information, the agent has to learn how to best select actions. Four discrete actions are available, corresponding to:

0 - move forward.
1 - move backward.
2 - turn left.
3 - turn right.
The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

# Dependencies
I solved this project in the Udacity Workspace. The dependencies are give [Here](https://github.com/udacity/deep-reinforcement-learning#dependencies)

# Train The Agent
Run parts 1. and 2. to intialize the environment. Skip part 3. Run part 4. to train the agent. <br>
<br>
This line in the training cell chooses configuration:<br>
agent = Agent(state_size=state_size, action_size=action_size, seed=0, *double = True, duelling=True* )<br>
double = True enables Double DQN<br>
duelling = True enables Duelling DQN<br>
<br>
The last network evaluates the performance over 10 iterations
