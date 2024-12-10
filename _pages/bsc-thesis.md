---
title: "Stock Trading using Actor-Critic RL"
permalink: /bsc-thesis/
author_profile: true
---
{% include base_path %}
\\
[[code](https://github.com/matinaghaei/Stock-Trading-ActorCriticRL)]

The usual methods used for financial trading are fundamental analysis, technical analysis, and algorithmic trading. Still, most of these methods can only predict prices, and they cannot explicitly make trading decisions or manage a portfolio.

The environment of financial trading consists of a state (prices and indicators), an action (opening/closing a position), and a reward (the profit). Therefore, it is easy to define the trading problem as a Markov decision process and use reinforcement learning algorithms to solve it. Actor-critic reinforcement learning algorithms allow us to manage a portfolio and adjust its positions directly.

In this project, we implemented three actor-critic deep reinforcement learning algorithms called A2C, DDPG, and PPO and used them for managing a portfolio consisting of the stocks in the Dow Jones Industrial Average. We compared the results with performances of two benchmarks, the buy & hold strategy and a random algorithm.

The RL algorithms are shown to outperform both benchmarks in terms of annual return, Sharpe ratio, and maximum drawdown. To ensure the consistency of the results, we repeated the experiment 50 times and calculated the p-values of the differences between the means of the results of each RL algorithm and the random algorithm.

A2C performance (The first row is an example of convergence, and the second row is not):

![](/images/plots-A2C.jpg)

DDPG performance (The first row is an example of convergence, and the second row is not):

![](/images/plots-DDPG.jpg)

PPO performance (The first row is an example of convergence, and the second row is not):

![](/images/plots-PPO.jpg)

The algorithms were tested 50 times. The table below shows the mean and standard deviation of the performances in terms of annual return, Sharpe ratio, and maximum drawdown:

![](/images/table1.png)

The p-values of the differences between the means of the results of each RL algorithm and the random algorithm were also calculated:

![](/images/table2.png)
