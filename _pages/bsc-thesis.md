---
title: "Portfolio Management Using Actor-Critic RL"
permalink: /bsc-thesis/
author_profile: true
---

{% include base_path %}

The usual methods used for financial trading are fundamental analysis, technical analysis, and algorithmic trading. Still, most of these methods can only predict prices, and they cannot explicitly make trading decisions or manage a portfolio. The environment of financial trading consists of a state (prices and indicators), an action (opening/closing a position), and a reward (the profit). Therefore, it is easy to define the trading problem as a Markov decision process and use reinforcement learning algorithms to solve it. Actor-critic reinforcement learning algorithms allow us to manage a portfolio and adjust its positions directly. In this project, we implement three actor-critic deep reinforcement learning algorithms called A2C, DDPG, and PPO and use them for managing a portfolio. We compare the results with performances of two benchmarks, the buy & hold strategy and a random algorithm. The RL algorithms are shown to outperform both benchmarks in terms of annual return, Sharpe ratio, and maximum drawdown. To ensure that the results are not random, we repeat the experiment 50 times and calculate the p-values of the differences between the means of the results of each RL algorithm and the random algorithm. [[code](https://github.com/matinaghaei/Stock-Trading-ActorCriticRL)]

A2C performance (the first row is converged and the second row is not converged):

![](/images/plots-A2C.png)

DDPG performance (the first row is converged and the second row is not converged):

![](/images/plots-DDPG.png)

PPO performance (the first row is converged and the second row is not converged):

![](/images/plots-PPO.png)

The algorithms were tested 50 times. The table below shows the mean and standard deviation of the performances in terms of annual return, Sharpe ratio, and maximum drawdown:

![](/images/table1.png)

The p-values of the differences between the means of the results of each RL algorithm and the random algorithm was also calculated:

![](/images/table2.png)
