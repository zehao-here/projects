---
layout: post-cutie
title: Thinking and Doing (II)
permalink: /cuties/think_do_2/
produced_at: 28 Oct 2025
---

## Story in One Paragraph

> The person who combines the two is the one who makes the connection. $[\dots]$ He understands how the yogis think and work. He knows the sort of ideas you can ask them to have and the sort you cannot. He knows the conditions and circumstances that are conductive to the production of ideas, and the sort that are inhibiting. He knows when they are genuinely stuck and when they are just slacking off.
>
<p style="text-align: right;">— Anthony Jay, <em>Management and Machiavelli</em></p>


## The New Role: Managers

In the previous post, we have seen how people with different skills can meet together and produce somewhat more efficiently ([here](/cuties/think_do/)). However, ideas from the thinkers or designers often seem too abstract or impractical for the doers to execute. For example, imagine smartphone designers come up with a sleek design: a phone with glass all the way to the edges and almost no borders. But when this idea reaches the factory, the engineers point out that details like how the glass bends, how wide the glue is, and how precisely pieces need to fit together make the phone easy to break and difficult to build. Clearly, a product manager is needed to bridge this gap.

We now introduce product managers to our model, which is termed as a `manager` between the thinkers and the doers. The job of a manager is to modify the intermediate good produced by the thinkers, making sure that it is conceivable or practical enough for the doers to execute. Accordingly, there comes to our model a new kind of intermediate goods that need to be produced after the *ideas* and before the final product. We call these intermediate goods *plans*. For a type $(s, e)$ individual, we assume that he can at most convert $\frac{1}{\lambda}se$ units of ideas into plans, $\lambda > 0$. This function form reflects the fact that coming up with a good bridging plan requires both thinking and doing skills. For ease of exposition, we continue to assume that everyone in the economy has $e \equiv 1$.

Let's make clear the production process. For a solo worker, we also assume that he needs to produce the plans. Indeed, even when someone acts alone, some forethought or planning is necessary before executing the final work. Thus, for an $(s, e)$ individual, the optimal speed of production is $\frac{1}{\frac{1}{s} + \frac{\lambda}{s} + 1} = \frac{s}{s + \lambda + 1}$. The meaning of the denominator is that producing one unit of final product requires $\frac{1}{s}$ units of time on thinking, $\frac{\lambda}{s}$ units of time on planning, and $1$ unit of time on doing.

<div class="image-single">
    <img src="{{ '/cuties/figs/think_do_2/solo_production.jpg' | relative_url }}" alt="Solo production" />
</div>

A firm now consists of n thinker, one or several managers and a number of doers. We continue to assume that the thinker is the employer competitively hiring managers and doers. The wage for a manager of a thinking level $s$ is denoted $w_m(s)$, and the wage for a doer of a doing level $e$ is denoted $w_d(e)$. Again, every individual in the economy can either be a thinker, a doer, a manager or a solo worker.

## Analysis

I have not completed formal proofs for the following results, but I hope the intuitions hold.

The employer (thinker) can always appropriate a positive share from one single final product, so he would produce $s$ ideas per unit of time, exploiting his thinking skills, and hire enough managers and doers. The number of managers is determined by the thinker's thinking level $s$ and their own speed of planning $\frac{s_m}{\lambda}$. Assuming homogenous managers in a firm, with a thinking level $s$ employer, the number of managers $n$ is given by $\frac{s}{n} / \frac{s_m}{\lambda} =  1$. In words, the thinking uses up the manager's time by giving him $\frac{s}{n}$ units of ideas per unit of time. The number of doers, since we have $e = 1$ for all people, is then $s$. 

We then naturally obtains a hierarchical firm, where due to the production sequence, the thinker is at the top, the managers are in the middle, and the doers are at the bottom.

<div class="image-single">
    <img src="{{ '/cuties/figs/think_do_2/firm_structure.jpg' | relative_url }}" alt="Firm structure" />
</div>
<p style="text-align: center;"><em>Figure: Hierarchy Structure in a Firm</em></p>

The equilibrium wage and occupational stratification can also be derived similarly. Intuitively, since individuals have homogenous doing, those who have relatively the least of thinking levels in the economy will become doers and receive a uniform wage, which amounts to the outside option value of the doer residing at the cutoff level ($\frac{s_1}{s_1 +\lambda +1}$, where $s_1$ is the cutoff level between doers and managers/thinkers). It's just like what happens in our previous model.

The wage for managers will be proportional to their thinking levels, which arises from the fact that a $2s_m$ manager just works as if there were two managers with $s_m$ thinking levels, and the competitive market drives the wage to be proportional. As a result, the wage function for managers take a simple form of $w_m(s) = \alpha s$. Also, remember that for the individual at $s_1$, he is indifferent between being a doer and a manager, so immediately we have $\alpha = \frac{1}{s_1 + \lambda + 1}$.

However, there seems to be no clear stratification between managers and thinkers. We have obtained the wages for managers. Taking one step further, you may find that the profit of employers (thinkers) is also given by $\pi(s) = \frac{s}{s_1 + \lambda + 1}$, which takes the same form as that for managers. To derive this, one can always calculate the profit of an employer with type $s$ when he hires $s$ doers and just enough managers of thinking level $s_1$. This calculation is always valid when we have homogenous doing and perfectly divisible managers.[^1]

Finally, it is interesting to see how the value of one single final product is distributed between the doers, managers and thinkers. With $e = 1$, each doer's share of a final product is exactly his wage, $\frac{s_1}{s_1 + \lambda + 1}$. A manager with type $s_m$ receives a wage of $\frac{s_m}{s_m + \lambda + 1}$, whereas he works with $\frac{\lambda}{s_m}$ units of ideas per unit of time (the inverse of his planning speed), so his share of one product is $\frac{\lambda}{s_m + \lambda + 1}$. The thinker gets the remaining $\frac{1}{s_1 + \lambda + 1}$ from one product.


<div class="image-single">
    <img src="{{ '/cuties/figs/think_do_2/share_allocation.jpg' | relative_url }}" alt="Value distribution of a final product" />
</div>
<p style="text-align: center;"><em>Figure: Value Distribution of a Final Product</em></p>


[^1]: If we allow heterogeneous doing, the picture might be slightly different, and we will discuss this in the next post.