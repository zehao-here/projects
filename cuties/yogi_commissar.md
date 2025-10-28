---
layout: post-cutie
title: Yogi and Commissar
permalink: /cuties/yogi_commissar/
produced_at: 16 Oct 2025
---

*The story/idea of Yogi and Commissar comes from Prof. [Jin Li](http://www.jin-li.org/). The modification I've made here is the introduction of thecomplexity level of a task along with the associated communication cost, which serves as a bridge explaining why Y and C dislike each other.*

*Update: I am no longer interested in using this to explain why Y and C dislike each other. But it may be still interesting to think of the complexity level as a bridge in some settings.*

## Story in One Paragraph

Yogi is a master thinker; Commissar, a champion of getting things done. On their own, each can tackle tougher (and more lucrative) tasks—the more thinking or doing, the more complex the job. Naturally, if you put their talents together, you'd expect productivity (and profits) to increase. And yes... only if they do not need to talk to each other.

## Model

**Skill.** Let $s$ denote the level of thinking skill possessed by one individual, and $e$ the doing skill. Yogi is good at thinking and has a type of $(s_1, e_1)$. Commissar, who is good at doing, has a type of $(s_2, e_2)$. We assume $s_1 > s_2$ and $e_1 < e_2$.

<div class="image-single" style="width: 50%;">
  <img src="{{ '/cuties/figs/yogi_commissar/fig1.jpg' | relative_url }}" alt="Skills: Yogi and Commissar" style="display: block; width: 100%; height: auto;" />
</div>

**Production.** There is abundant good of varying complexity levels to choose and produce. A good of complexity level $k \in [0, \infty)$ is valued at $vk$. A more complicated task requires more costs, while good thinking and doing skills can help reduce the costs. Formally, the thinking cost is $\frac{k^2}{2s}$, and the doing cost is $\frac{k^2}{2e}$. As a result, for an individual with type $(s, e)$, the total profit of producing a good of complexity level $k$ is $vk - \frac{k^2}{2s} - \frac{k^2}{2e}$.

Yogi and Commissar work together to produce a good. Now the associated thinking and doing costs are determined by whoever has the higher skill. However, a communication cost $\frac{1}{2}\lambda k^2$ is incurred for team production.

## Analysis

Let's see what happens if Yogi and Commissar work on their own. Calculating the first order condition will quickly offer us the optimal good complexity for Yogi as a solo worker, which is $k_Y^* = 1/(\frac{1}{s_1} + \frac{1}{e_1})v$. The profit is $\frac{1}{2}(\frac{1}{s_1} + \frac{1}{e_1})v^2 = \frac{1}{2}k_Y^*v$. We can calculate similar things for Commissar.


When they work together, the optimal good complexity is $k_T^* = 1/(\frac{1}{s_1} + \frac{1}{e_2} + \lambda)v$. Commissar's skill in doing help reduce the doing cost, which is beneficial for team production. However, the communication cost is now present. The profit is $\frac{1}{2}(\frac{1}{s_1} + \frac{1}{e_2} + \lambda)v^2 = \frac{1}{2}k_T^*v$.

If the communication cost plays a vital role here, i.e., $\lambda \geq \frac{1}{e_1} - \frac{1}{e_2}$, then we actually have $k_T^* < k_Y^* $. The optimal complexity of the good produced under team production is weakly lower than that produced by Yogi alone. Similarly, if $\lambda \geq \frac{1}{s_2} - \frac{1}{s_1}$, then we have $k_T^* < k_C^*$. If we further assume that team production operates at a speed twice of solo production, while Yogi and Commissar evenly split the profit, then in this case, Yogi and Commissar would prefer to work separately.

## Remarks

The trick I've put in this version of the Yogi and Commissar story is to use the complexity level as a bridge. Yogi and Commissar dislike each other but not just because they are so different. Team production creates communication costs, which increase with the complexity level of the good to be produced. It might be an economically rational decision for them to work separately.

One could imagine that, the introduction of a new player, the manager who might be able to reduce the communication cost, preserves the team production. An easy way to model this is to let the manager decrease the parameter $\lambda$ to some lower $\lambda'$. But is there a more interesting way to model this?
