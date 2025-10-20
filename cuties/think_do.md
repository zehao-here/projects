---
layout: post-cutie
title: Thinking and Doing
permalink: /cuties/think_do/
produced_at: 15 Oct 2025
---

## Story in One Paragraph

Some people have a lot of ideas but lack the time to ship them, while others, relatively, just experience fewer sparks but get things done. To ease this bottleneck, it's natural to put them working together. Our model shows how the division of labor and the wages that come with it can emerge endogenously in this setting. It also explores how AI, as either in the form of augmentation or substitution, can affect the economy.

## Model

We consider a simple version where all individuals have the same level of doing here. The model can be easily extended to allow heterogeneous doing levels, but in general that does not add additional insights.

**Skills.** There is one unit of individuals living in the economy. Each individual's type is denoted by $(s, e)$, where $s$ is the thinking level and $e$ is the execution/doing level. We assume $e \equiv 1$ for all individuals. The distribution of thinkings is denoted by $F$, which is continuous and has a decreasing density $f$ fully supported on $[0, \infty)$. In addition, we assume $F(0) = 0$ and $\mathbb{E}[s] < \infty$.

**Production.** In a unit time, an individual with type $(s, e)$ can either produce $s$ units of intermediate good, or he can convert at most $e$ units of intermediate good into $e$ units of final good. No final good can be produced if there is no intermediate good at hand. If an individual produces on himself (a `solo worker`), the optimal speed of production is $\frac{s \cdot 1}{s+1}$. To see this, optimal production needs thinking and doing balanced, so for an $(s, 1)$ individual, he should assign his time to think and execute in the ratio of $1$ to $s$. It's easy to imagine that, relatively, a one-legged individual does not produce quickly.

We allow individuals to set up `firms` to work together. Each firm is made up of one `employer` who specializes in thinking and a number of `employees` who specialize in doing. Each individual is free to choose his role in the economy, where he may either be an employer, an employee or a solo worker. However, an employer needs to pay wages to his employees to attract them. Each individual can freely offer any wage to any other individual, who may then choose to accept or reject the offer.

**Payoffs.** The intermediate good values zero. The value of the final good is normalized to be 1. An employer's payoff is his profits, which is the value of the final goods his firm produces minus the wages he pays to all his employees. An employee's payoff is his wage. A solo worker's payoff is the value of the final goods he produces. Thinking and doing has no costs. There are also no other costs, e.g., setting up a firm, finding employees, etc.

## Equilibrium

It's very interesting to mention one classic model, Lucas (1978)[^1], with which our model shares many similar spirits though not rational expectations here. Similar to that model, the equilibrium here is also pinned down by two conditions. Firstly, the individual in the "middle" is indifferent between being hired, hiring people or working alone. Secondly, the measure of total thinkings from employers and doings from employees should be equal in equilibrium.

Let's first discuss the wages in the equilibrium, which turns out to be uniform across the employees. One trick I have used in developing the model is that, thinking and doing are separately conducted. As a result, in a firm with the thinking-doing division, an employer is entirely indifferent between hiring $(\frac{1}{10}, 1)$ or $(2, 1)$, as what matters is only the level of doing for employees - but everyone is homogeneous in doing. Recall that firms also compete for employees, so the equilibrium wage must be the same for all employees.

Now the indifference condition. Because we have let the employers specialize in thinking, those with relatively higher thinking level prefer hiring people, while those with relatively lower thinking level prefer being hired. The logic of comparative advantage. Will there be any solo workers? There could be, but only in a set of measure zero. Intuitively, only individuals with a moderate level of thinking ability would consider working solo. However, even for them, it is always more profitable to hire others and become an employer, since they can delegate execution to workers at a lower cost instead of doing it themselves (and then enjoy their relatively higher thinking levels). As a result, on the positive real line of thinking levels, people on the left-hand side become doers and people on the right are thinkers. The equilibrium wage is the outside option value of the indifferent individual.

The exact location of the indifferent individuals (along with the equilibrium wage) is pinned down by the market clearing condition. In the equilibrium, every firm has sufficient employees (equal to the employer's thinking level) to produce. The total measure of execution by all doers should be equal to the total measure of thinking by all thinkers. It also can be proved that there always exists such a cutoff as long as $\mathbb{E}[s] < \infty$. The following figure illustrates the equilibrium.

<div class="image-single">
    <img src="{{ '/cuties/figs/think_do/fig1.png' | relative_url }}" alt="Equilibrium" />
</div>

## The Impact of AI

How will the advent of AI affect the economy? It turns out that it depends on what kind of AI we have. Following the recent discussion, I consider two types of AI, `augmentation` or `substitution`.

### Augmentative AI

The augmentative AI is modelled as uniformly increasing everyone's doing level from $1$ to $\gamma > 1$. With augmentation, more people now become thinkers. However, it turns out that whether equilibrium wage will increase depends on the magnitude of $\gamma$ and the shape of the distribution of thinking. There are two effects of augmentation. The first effect is that, the indifferent individual now has a relatively lower thinking level, so his outside option value is lower compared with the indifferent individual in the pre-AI equilibrium. However, augmentative AI increases everyone's outside option value. In general, for an $F$ with a decreasing density, a fatter right tail will lead to an increase in equilibrium wage. It can be checked that $F(s) = 1 - \frac{1}{(1+s)^2}$ can generate this.

### Substitutional AI

The substitutional AI is modelled as a pool of computations available to firms, which is quantitatively equal to a measure of $\mu < (\int_{0}^{\infty} s f(s) ds)$ execution resources. Firms bid for using the computations, and the unit price of computation will be equal to the labor wage in equilibrium. Because human doers can be replaced by AI, we have fewer doers in the economy. In terms of wage, it turns out that, regardless of the shape of $F$, the equilibrium wage will always decrease because only the first aforementioned effect happens. Those employers with high thinking levels will profit from a lower equilibrium wage.

The following figure illustrates the equilibrium with augmentative and substitutional AI.

<div class="image-row">
    <img src="{{ '/cuties/figs/think_do/fig2.png' | relative_url }}" alt="Augmentative AI" />
    <img src="{{ '/cuties/figs/think_do/fig3.png' | relative_url }}" alt="Substitutional AI" />
</div>


## Remarks

One feature of the current model is that there is no effective matching between people, even if we allow people to also differ in doing. Inside firms, we do not have structures or interactions between people either. 

It could be a problem, also a way out, that the final output in this model is indeed homogeneous. I am considering a new economy with diverse complexities of tasks, and people with higher thinking or doing may be more efficient in producing more complicated tasks which also produce more values. It might generate interesting matching between people and hierarchical structure within firms.






[^1]: Lucas Jr, R. E. (1978). On the size distribution of business firms. *The Bell Journal of Economics*, 508-523.
