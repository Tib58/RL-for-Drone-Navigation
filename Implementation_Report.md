# Report


This report outlines the design choices and challenges encountered during the development of the Drone Navigation simulation.


# Design Choices

Environment Setup

1. Grid-based Simulation:

The grid provides a simple and intuitive way to visualize the agent's learning process and actions. It simplifies the observation and action spaces, making it ideal for educational purposes and initial experiments in reinforcement learning.

Implementation: The environment uses a two-dimensional grid where the drone's position and the target are defined by coordinates. The drone navigates the grid to reach the target.

2. Action and Observation Space:

Action Space: The drone can move in four directions—up, down, left, and right. 

Observation Space: Composed of the drone's and the target's coordinates, it encapsulates all necessary information for the drone to learn how to navigate effectively.

3. Reward System:

The reward system is designed to teach the drone efficiency. The drone receives a high reward for reaching the target and a small penalty for each move to encourage finding the shortest path.

Implementation: A reward of 100 is given for reaching the target, and a penalty of -1 for each step taken.

# Use of Stable Baselines3's PPO

Choice of PPO: Proximal Policy Optimization is known for its effectiveness and stability in a variety of environments, making it an excellent choice for training policies in new and potentially complex simulations.

# Challenges Faced
1. Balancing Complexity and Usability:

Issue: Ensuring the simulation is both accessible to beginners and rich enough to provide meaningful insights into RL was challenging.

Approach: Opted for a simple grid and straightforward tasks to keep the barrier to entry low while allowing for deeper exploration through parameter tuning and extended training options.

2. Visualization Limitations:

Issue: Maintaining clear and informative visual feedback during training sessions without slowing down the simulation or overwhelming the user was difficult.

Approach: Implemented a basic visualization using matplotlib to provide real-time feedback on the drone's position and the grid, which can be turned off to speed up training sessions.

3. Parameter Tuning:

Issue: Finding the right balance of environmental parameters (like step penalties and rewards) that would consistently lead to effective learning was time-consuming.

Approach: Conducted multiple training runs with different settings, analyzing the performance to adjust the parameters accordingly.

# Improvements and Extensions
Given more time and resources, several improvements and extensions could be considered:

1. Enhanced Observation Space:
Proposal: Include additional features such as obstacles or varying terrain to enrich the environment and introduce more complex navigation challenges.

2. Advanced Visualization Tools:
Proposal: Develop more sophisticated visualization tools to better analyze and interpret the agent’s behavior over time.

3. Real-World Application Simulation:
Proposal: Adapt the simulation to mimic real-world scenarios, to provide practical insights and applications for RL strategies.
