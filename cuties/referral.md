---
layout: post-cutie
title: Recommending My Friend
permalink: /cuties/referral/
produced_at: 26 Nov 2025
---

## Story in One Paragraph

People would like to recommend their friends instead of who are more capable.

## Model

We have one principal, two groups (A and B), and two agents (1 and 2) here. The principal must select one of the two agents to conduct a project. Groups A and B can recommend which agent the principal should choose.

Agent 1 has higher ability than agent 2, represented by their types $\theta_1 > \theta_2$ with $\theta_1, \theta_2 \in (0,1)$. The groups observe agents’ abilities perfectly. The principal does not know the agents' types.

The recommendation is captured by two parameters, $m_1$ and $m_2$, where $m_1, m_2 > 0$ and $m_1 + m_2 = \tfrac{1}{2}$. These can be understood as the endorsement power of the two groups. If both groups recommend agent 1, then agent 1 is chosen with probability $\frac{1}{2} + m_1 + m_2 = 1$, so agent 2 is never selected. If group A recommends agent 1 while group B recommends agent 2, then agent 1 is selected with probability $\tfrac{1}{2} + m_1 - m_2$, and agent 2 is selected with probability $\tfrac{1}{2} - m_1 + m_2$.

Agent 1 is group A's friend, and agent 2 is group B's friend. If the selected agent is a group’s friend, that group enjoys a personal benefit $b > 0$. In addition, both groups care about project success: a successfully conducted project yields payoff $\pi > 0$ to each group. The principal cares only about whether the project succeeds.

## Analysis

Group A will unambiguously recommend agent 1, since agent 1 both has higher ability and is A's friend. Group B has to strategically determine its choice between the two agent. Standing in the shoes of group B, B has the following considerations:

Supporting agent 1: agent 1 will be selected for sure. B enjoys a better chance of a successful project, but loses its personal benefit $b$.

Supporting agent 2: with a positive probability, the weaker agent 2 will be selected, and offers group B a personal benefit. However, the probability of a successfully conducted project is decreased.

It turns out that the optimal strategy for group B is to support agent 2 if $b \geq (\frac{1}{2} - m_1 + m_2)(\theta_H - \theta_L)\pi$. A sufficiently large personal benefit will make group B support its friend, harming the project's success.


