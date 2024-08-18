# Solving Gymnasium’s Car Racing with Reinforcement Learning

## Soft-Actor Critic (SAC)

![](/Images/sac_car_racing.gif)

## Deep Q Learning (DQN)

![](/Images/dqn_car_racing.gif)

## Proximal Policy Optimization (PPO)

![](/Images/ppo_car_racing.gif)

## Results
Hardware: Google Colab T4 High-RAM

| Model Type | Discrete | Average Reward| Training Time | Total Training Steps |
|------------|----------|---------------|---------------|----------------------|
| PPO        | No       | 766.83        |  3:39:20      | 399,999              |
| SAC        | No       | -21.16        |  3:12:53      | 100,000              |
| DQN        | Yes      | 811.63        |  4:23:17      | 501,234              | 

## Training Notes
- Set `ent_coef` for PPO as it encourages exploration of other actions. Stable Baselines3 defaults the value to 0.0. [More Information](https://www.youtube.com/watch?v=1ppslywmIPs)
- Do not set your `eval_freq` too low, as it can sometimes cause instability during learning due to being interrupted by evaluation. (e.g. >=10,000)
- `buffer_size` defaults to 1,000,000, which requires significant memory for DQN and SAC. Try setting it to a more practical amount (e.g. 200,000)

## Finding Theta Blog Posts:
 - [Solving Gymnasium's Car Racing with Reinforcement Learning](https://www.findingtheta.com/blog/solving-gymnasiums-car-racing-with-reinforcement-learning)
