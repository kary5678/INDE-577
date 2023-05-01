# Reinforcement Learning

Reinforcement learning is a type of machine learning where an agent learns how to make decisions through trial and error by interacting with an environment. The goal of reinforcement learning is to maximize a cumulative reward signal over time. In terms of the data, it is not labeled like in supervised learning, but it is not completely unlabeled either. The environment provides feedback in the form of rewards and observations, which the agent uses to update its policy or strategy for taking actions and serves as a form of supervision.

The basic components of reinforcement learning are the:

* **Environment:** external system with which the agent interacts
* **State:** the state of the environment is the information that is used to describe the current situation, usually represented as a set of features or variables
* **Action:** the decision that the agent makes based on the current state
* **Reward:** the feedback that the agent receives after taking an action, indicating how good or bad the action was in terms of achieving the goal of the task
* **Policy:** the strategy that the agent uses to determine its actions based on the current state

### Applications

Reinforcement learning has a wide range of applications in various fields, such as:

* Game playing: develop agents that can play complex games such as Go (remember AlphaGo?), chess, and poker at a superhuman level
* Robotics: train robots to perform complex tasks such as grasping objects, walking, and flying
* Recommendation systems: optimize the recommendations given to users based on their actions and feedback
* Control systems: optimize the control of complex systems such as power grids and traffic systems

### Evaluation Metrics

In reinforcement learning, the performance of an agent is typically evaluated using one or more of the following metrics:

* **Cumulative reward:** the sum of rewards received by the agent over a period of time
* **Discounted cumulative reward:** the sum of rewards received by the agent over a period of time, discounted by a factor that reflects the importance of immediate versus future rewards
* **Convergence:** the rate at which the agent learns to make better decisions over time, measured by plotting the average reward received by the agent over time

One of the challenges in reinforcement learning is the exploration-exploitation dilemma. The agent must decide whether to explore new actions that may lead to better rewards in the long term or to exploit the actions that have already been found to lead to good rewards in the short term. One heuristic to balance exploration and exploitation is the epsilon-greedy policy, where the agent selects the action with the highest expected reward with probability 1-epsilon and selects a random action with probability epsilon.

## Directory Contents

We only briefly discussed reinforcement learning methods in class, and are not expected to implement them. I have included subdirectories with a `README.md` for their respective algorithm and their application. Visit their respective links below:

1. [***k*-Armed Bandit**](https://github.com/kary5678/INDE-577/tree/main/reinforcement-learning/k-armed_bandit) - classical reinforcement learning problem where an agent must choose between k different actions (or arms) to maximize the cumulative reward over time
