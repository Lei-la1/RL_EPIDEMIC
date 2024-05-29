# RL_EPIDEMIC :syringe:

### Abstract 
This project focuses on implementing a vaccination strategy using reinforcement learning to stop the spread of a disease. In our environment, an agent moves across a grid and decides whether to vaccinate individuals. The grid represents people who can be in one of four states: susceptible, infected, vaccinated, or recovered (SIRV). We employed various RL algorithms, including PPO, DQN, and REINFORCE, to observe the emergence of strategies. While we successfully solved the problem using PPO, we encountered more difficulties with DQN and REINFORCE.

### Environment
The environment is represented as a three-dimensional grid with dimensions corresponding to channels (C), height (H), and width (W). Each cell within this grid can occupy one of four possible states: susceptible (S), infected (I), recovered (R), or vaccinated (V). We use four channels to encode the state of each cell. 

SRIV: Susceptible, Recovered, Infectious, Vaccinated 
- (1,0,0,0) -> You are susceptible, you can get the disease and need vaccination
- (0,1,0,0) -> You are infectious and sick, you can pass on the disease to your neighbors, its too late for vaccination
- (0,0,1,0) -> You are recovered, after being infectious, you cannot cannot pass on the disease 
- (0,0,0,1) -> You are vaccinated, you cannot become infected and cannot propagate the disease

### Action Space
The agent has a discrete set of five actions

A = { move right, move left, move up, move down, vaccinate}


### Set up
pip install -r requirements.txt
