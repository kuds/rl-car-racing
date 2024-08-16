# Solving Gymnasium’s Car Racing with Reinforcement Learning

## Soft-Actor Critic (SAC)

![](/Images/sac_car_racing.gif)

## Deep Q Learning (DQN)

![](/Images/dqn_car_racing.gif)

## Proximal Policy Optimization (PPO)

![](/Images/ppo_car_racing.gif)

## Results
Hardware: Google Colab T4

| Model Type | Discrete | Average Reward| Training Time | Total Training Steps |
|------------|----------|---------------|---------------|----------------------|
| PPO        | No       | 347.60        |  1:32:55      | 80,000               |
| SAC        | No       | -21.16        |  3:12:53      | 100,000              |
| DQN        | Yes      |               |               |                      |

## Training Note
- Set ent_coef for PPO as it encourages exploration of other actions. Stable Baseline3 defaults the value to 0.0. [More Information](https://www.youtube.com/watch?v=1ppslywmIPs)
- Do not set your eval_freq too low, as it can sometimes cause instability, as the evaluation might interrupt the learning process. Try increasing the eval_freq to a higher value (e.g., 10,000) to reduce the potential disturbance to learning.

## Finding Theta Blog Posts:
 - [Solving Gymnasium's Car Racing with Reinforcement Learning](https://www.findingtheta.com/blog/solving-gymnasiums-car-racing-with-reinforcement-learning)
