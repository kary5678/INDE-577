# The k-Armed Bandit Problem

The k-armed bandit problem is a classical reinforcement learning problem in which an agent must choose between k different actions (or arms) to maximize the cumulative reward over time. The agent must make a decision at each time step and receive a reward based on the action taken. The goal is to learn the best action to take in order to maximize the total reward received.

## Algorithm

1. Initialize the action-value estimates for each arm to zero, $Q(a) = 0$

2. For each time step t:

    a. Choose an arm to play based on a *policy* (e.g., $\epsilon$-greedy, softmax, etc.)
    
    b. Receive a reward, $R_t$, from the chosen arm
    
    c. Update the action-value estimate for the chosen arm based on the reward received, $Q_t(a) \leftarrow Q_{t-1}(a) + \alpha(R_t - Q_{t-1}(a))$, where $\alpha$ is the learning rate
    
3. Repeat step 2 until the desired number of time steps have been reached or a convergence criterion has been met

### Breaking it down

At each time step, the agent must choose an action to take. This is done using a policy, which defines how the agent selects an action given the current estimates of the action-values. For example, a simple $\epsilon$-greedy policy would select the action with the highest estimated action-value with probability $1-\epsilon$ and select a random action with probability $\epsilon$.

After the action is chosen and the reward is received, the agent updates the action-value estimate for the chosen action using a simple update rule. The update rule is a form of incremental learning, where the estimate for each action is updated based on the reward received and the previous estimate for that action. The learning rate $\alpha$ controls how quickly the estimates are updated.

The goal of the algorithm is to learn the action-values for each arm, so that the agent can choose the action with the highest value in order to maximize the expected reward.

## Advantages/Disadvantages

✓ Simple and easy to implement

✓ Can handle non-stationary problems (i.e., when the true values of the actions change over time)

✓ Can balance exploration (trying new actions) and exploitation (choosing the best action)

✗ Can be slow to converge and may require a large number of time steps to learn the optimal action-values

✗ Can suffer from the exploration-exploitation dilemma, where the agent may get stuck exploring too much and miss out on potential rewards

✗ Assumes that the reward for each action is independent of the actions taken in the past, which may not be the case in some problems.

## Implementation on Dataset

While we discussed this algorithm in class, we were not expected to implement it.
