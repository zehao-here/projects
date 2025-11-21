---
layout: post-cutie
title: Please the Difficult Boss
permalink: /cuties/new_contents/
produced_at: 21 Nov 2025
---

## Story in One Paragraph

Minister Hacker and Sir Humphrey — a week ago comrades - now enroll in a policy fight. Both are strutting around like they own the place. Unfortunately, our poor Bernard needs to decide the position of the policy today, which may either drive Hacker or Humphrey unhappy. Bernard realizes that staying neutral initially is the name of the game, though slightly leaning to one more likely to win later. More importantly, also to the boss who is much harder to appease later.

## Model

Our game has an agent, **Bernard**, and two principals, **Hacker ($L$)** and **Humphrey ($R$)**. The principals have diverse utilities: Hacker prefers $\theta_L = -1$ and Humphrey prefers $\theta_R = 1$.

There are two periods in the game. In the first period, the fight between Hacker and Humphrey is so fierce that it is impossible for Bernard to know who will win. However, Bernard holds a prior belief $\alpha \in (0,1)$ that the winner is Hacker. In period $t=2$, the identity of the winner, which is Bernard's true principal, is revealed. In each period, Bernard adopts the utility of the true principal, which takes the quadratic loss form $-(y_t - \theta)^2$. 

Bernard has to choose a project to implement in each period. When he has made a choice $y_1$ in period 1, it incurs a cost for him to deviate to another project $y_2$ in period 2. We model this as $c(y_1, y_2) = c_i (y_2 - y_1)^2$, where $c_i > 0$, $i \in \lbrace L, R \rbrace$ represents the difficulty of moving toward a specific direction. Formally, we have

\[
c(y_1, y_2) = \begin{cases}
c_R(y_2 - y_1)^2 & \text{if } y_2 \geq y_1 \text{ (Moving Right)} \\
c_L(y_2 - y_1)^2 & \text{if } y_2 < y_1 \text{ (Moving Left)}
\end{cases}
\]

## Analysis

### Case 1: Symmetric Costs
First, consider the baseline where the difficulty of adjusting the project is identical regardless of direction ($c_L = c_R = c$).

We solve the problem backward. In Period 2, Bernard knows the identity of the boss. He tries to align with the boss's preferred action ($\theta$) but is held back by his previous decision ($y_1$). It turns out that, by attacking the FOC, we have:
\[
y_2^{\ast}(\theta_1) = \frac{c y_1 - 1}{1 + c}
\]
Then we enter to the analysis of period 1. The first period optimization problem can be solved by first spelling out Bernard's value functions in period 2 contingent on state realization, and them plug them back. It can be found that Bernard's optimal choice in period 1 is $y_1^{\ast} = 1 - 2\alpha$, irrelevant of the cost $c$.

Intuitively, since the cost $c$ is symmetric, the "pain" of being wrong about Hacker is mathematically identical to the "pain" of being wrong about Humphrey. Bernard's only optimal strategy is to stay neutral initially, and his position is purely based on his prior belief $\alpha$.

The optimal second-period choices can be found as $y_2^\ast(L) = - 1 + \frac{2c(1-\alpha)}{1+c}$ and $y_2^\ast(R) = 1 - \frac{2c\alpha}{1+c}$. When $c \to 0$, $y_2^\ast(L) \to -1$ and $y_2^\ast(R) \to 1$. That is, the second-period choices are always aligned with the preferred actions of the two bosses. When $c \to \infty$, $y_2^\ast(L) \to 1 - 2\alpha$  and $y_2^\ast(R) \to 1 - 2\alpha$. Bernard essentially never revises.


### Case 2: Asymmetric Costs (Pre-emptive Hedging)
Now, suppose that "moving Left" (toward Hacker) is harder than "moving Right" (toward Humphrey). We denote the cost of moving left as $c_L$ and the cost of moving right as $c_R$, where $c_L > c_R$.

We define a "rigidity factor" for each direction as $K_i = \frac{1+2c_i}{1+c_i}$. Since $c_L > c_R$, it follows that $K_L > K_R$. Bernard's optimal period 1 choice becomes
\[
y_1^{\ast} = \frac{(1-\alpha)K_R - \alpha K_L}{(1-\alpha)K_R + \alpha K_L}
\]
This reveals a strategic bias. If we assume Bernard is completely uncertain ($\alpha = 0.5$), the numerator becomes proportional to $K_R - K_L$. Since moving left is harder ($K_L$ is larger), the numerator is negative, implying $y_1^{\ast} < 0$.

Bernard engages in **pre-emptive hedging**. He positions the initial project closer to Minister Hacker ($L$). The intuition is that if Hacker takes power, Bernard is already safely nearby and avoids the expensive $c_L$ adjustment. If Sir Humphrey takes power, Bernard is far away, but the cost to move right ($c_R$) is cheap enough to be manageable. Thus, asymmetric friction leads to biased initial decision-making, even with a neutral agent.