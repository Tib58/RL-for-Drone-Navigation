# RL-for-Drone-Navigation

# Overview

This Drone Navigation simulation employs a custom Gymnasium environment to train a drone to navigate towards a target location on a grid. The project uses the Proximal Policy Optimization (PPO) algorithm from the Stable Baselines3 library for training an agent (the drone) to learn optimal paths based on the environment's rewards and penalties. 


# Requirements

Ensure you have Python 3.6 or newer and pip installed on your system. The project is a Jupyter Notebook file.

# Run

Execute the notebook cell.
During initialization, you will be prompted to enter simulation parameters such as grid size, number of steps, and target positions. You can also use the default values.

# Environment and Agent Details

DroneNavigation Environment
Action Space: The agent chooses from four discrete actions: move up (0), move down (1), move left (2), and move right (3).
Observation Space: Observations include the drone's current position and the target position, expressed as a vector of four integers.
Rewards: The drone receives a reward of 100 for reaching the target and a penalty of -1 for each step taken, encouraging efficiency.
PPO Algorithm
The Proximal Policy Optimization (PPO) algorithm is utilized for training the agent. PPO is a policy gradient method for reinforcement learning which optimizes a surrogate objective function and uses a clipped objective to prevent large policy updates, enhancing stability.

Training: The agent trains for a specified number of timesteps (default is 50,000), learning to optimize its path to the target over successive episodes.


# Visualization

The simulation supports visual rendering in 'human' mode, where the drone's movements are animated on a grid. 
