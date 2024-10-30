# Multi-Armed-Bandit
The multi-armed bandit problem is a classic dilemma in decision-making under uncertainty. It gets its name from the traditional "one-armed bandit" slot machines, where gamblers pull a lever (the "arm") to potentially win a prize. In the multi-armed bandit problem, we extend this scenario to multiple slot machines (or "arms"), each with an unknown payout distribution. The objective is to develop a strategy that maximizes rewards over time by deciding which arm to pull based on past outcomes and balancing the exploration of new options with the exploitation of known rewards.

## Problem Analogy and Goal
To understand the multi-armed bandit problem, consider a gambler in a casino faced with several slot machines, each with a different, unknown payout rate. The gambler's goal is to maximize the total reward over a series of lever pulls by choosing which machines (or "arms") to play. The challenge lies in the fact that each arm has an unknown probability distribution of rewards, and the only way to learn about an arm's reward probability is by pulling it and observing the outcome.

This problem introduces a fundamental trade-off between exploration and exploitation: the gambler must decide between trying out different machines to discover which has the best payout (exploration) and focusing on machines that have historically paid well (exploitation).

## Mathematical Model and Objective Function

In the mathematical formulation of the multi-armed bandit problem, each arm's reward structure is represented as a probability distribution, showing the expected reward for each option. The objective is to find an optimal policy \( \pi \) that maximizes the expected sum of rewards over time. Formally, we aim to maximize the following function:

\[
\max_{\pi} \mathbb{E} \left[ \sum_{t=1}^{N} r_t \right]
\]

Here:
- \( r_t \) represents the reward at time \( t \), which is the outcome of choosing one of the arms at that time.
- The policy \( \pi \) is the strategy for deciding which arm to pull at each time step, balancing exploration and exploitation.

The goal of an effective policy is to minimize regret, which is the opportunity cost of not knowing each arm’s potential rewards immediately. Regret measures how much we lose by learning about each arm gradually instead of knowing its payout rate from the start.
