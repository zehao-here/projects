---
layout: post
title: "AI, Headquarters and Guijie"
categories: [cuties]
---

# AI, Headquarters and Guijie

## Model

- Two players: a headquarter (P) and a guijie (A). P initiates a campaign to boost sales. A successful campaign first depends on the market condition $\theta \in \{0, 1\}$, which P does not know well. With probability $q \in (0, 1)$, the campaign may be initiated at a time when the market is actually bad ($\theta = 0$). With probability $1-q$, the campaign is initiated at a correct time, i.e., $\theta = 1$. Guijie observes a noisy signal $s$ with $\Pr(s=1\mid \theta=1)=1$ and $\Pr(s=1\mid \theta=0)=p\in(0,1)$.
- The second component of success is the guijie's effort $e \in \{0, 1\}$. Guijie bears a cost of $c$ if $e = 1$, no cost if $e = 0$.
- The final outcome of the campaign is $y \in \{0, 1\}$, and $y = \theta e$. P receives a payoff of $\Pi_P$ if $y = 1$, and zero otherwise. Guijie does not profit directly from the campaign. To incentivize guijie to work, P offers a bonus $b$ to A if $y = 1$. Both P and A are risk neutral.
- Timing:
  1. P initiates the campaign and signs the bonus contract $b$ with A.
  2. Market condition $\theta$ realizes. Guijie observes $s\mid \theta$ and decides whether to exert effort $e$.
  3. P and A observe $y$ and receive their payoffs.

## Analysis

- Suppose $\Pi_P$ is large enough. Upon observing $s=1$, the posterior of $\theta$ is $\Pr(\theta=1\mid s=1)=\frac{1-q}{1-q+pq}$. A chooses $e = 1$ iff $\frac{1-q}{1-q+pq} b - c \geq 0$.
- If A has a relatively poor signal ($p$ large), the bonus $b$ must be large enough to compensate the effort cost spent on a bad market. If the advent of AI improves the signal of A (i.e., a lower $p$), the bonus $b$ can be made smaller.
- Note that $\frac{1-q}{1-q+pq}$ is also decreasing in $q$. As a result, with the possible aid of AI, if P is more likely to initiate the campaign at a good time, a lower bonus $b$ will be sufficient to incentivize A to work.

