---
layout: post-cutie
title: Thinking and Doing (II)
permalink: /cuties/think_do_2/
produced_at: 28 Oct 2025
---

*Update: The production function of managers is modified. Contents are also polished for better readability. (Dec 3, 2025)*

## Story in One Paragraph

> The person who combines the two is the one who makes the connection. $[\dots]$ He understands how the yogis think and work. He knows the sort of ideas you can ask them to have and the sort you cannot. He knows the conditions and circumstances that are conductive to the production of ideas, and the sort that are inhibiting. He knows when they are genuinely stuck and when they are just slacking off.
>
<p style="text-align: right;">— Antony Jay, <em>Management and Machiavelli</em></p>


## The New Role: Managers

In our previous post, people with different skills meet together and produce more efficiently ([here](https://zehao-here.github.io/projects/cuties/think_do/)), a fairy tale about comparative advantage. We continue the fairy tale by introducing a new character, the `manager`, in our story.

Ideas from thinkers often seem too abstract or impractical for doers to execute. A well-known example comes from Boeing’s 777 program in the early 1990s. Top executives and airline customers agreed on a memo that promised a “truly great airplane” with the best dispatch reliability and customer appeal in the industry, plus new technologies like fly-by-wire controls and a fully digital design—all on an aggressive schedule. Engineers and factory teams worried that this wish-list was unrealistic, especially given Boeing’s old way of working, where designers threw drawings “over the wall” and left manufacturing to fix the problems late in the process. Alan Mulally, the program manager, and a layer of design-build team leaders then acted as middle managers: they formed cross-functional teams that co-located designers, production engineers, suppliers and airline representatives and negotiated trade-offs between the grand vision and what the doers could actually build. Boeing's success in the 777 program is largely attributed to the effective coordination of these middle managers.[^1]

Back to our model. A (product) `manager` now stands between the thinker and the doer. The job of a manager is to modify the intermediate good produced by the thinkers, making sure that it is conceivable or practical enough for the doers. Accordingly, we assume in our model a new kind of intermediate goods that need to be produced after the ideas and before the final product. We call these intermediate goods `manuals`. For a type $(s, e)$ individual, we assume that he can at most convert $\frac{1}{\lambda}\sqrt{se}$ units of ideas into manuals, $\lambda > 0$. This function form reflects the fact that coming up with a good bridging manual requires both thinking and doing skills. For ease of exposition, we continue to assume that everyone in the economy has $e \equiv 1$.

Let's make clear the production process. We assume that a solo worker still needs to produce the manuals. Indeed, some forethought or planning is necessary even if one works alone. For an $(s, e)$ solow worker, the maixmal speed of value creation (which values $1$) is $\frac{1}{\frac{1}{s} + \frac{\lambda}{\sqrt{s}} + 1}$. The denominator means that to produce one unit of final product requires $\frac{1}{s}$ units of time optimally allocated to thinking, $\frac{\lambda}{\sqrt{s}}$ units of time to producing a manual, and $1$ unit of time optimally allocated to doing.

<div class="image-single">
    <img src="{{ '/cuties/figs/think_do_2/solo_production.jpg' | relative_url }}" alt="Solo production" />
</div>
<p style="text-align: center;"><em>Figure: Solo Production Process</em></p>

A firm consists of one thinker, several managers and a number of doers. We continue to assume that the thinker is the employer competitively hiring managers and doers, so she always has perfect bargaining power. The wage for a manager of a thinking level $s$ is denoted $w_m(s)$, and the wage for a doer of a doing level $e$ is denoted $w_d(e)$. Every individual in the economy freely chooses his role, which can be either a thinker, a manager, a doer or a solo worker.

## Analysis

I have not completed formal proofs for the following results, but I hope the intuitions hold.

The employer (thinker) can always appropriate a positive share from one single final product, so he would produce $s$ ideas per unit of time, exploiting his thinking skills, and hire enough managers and doers. Assuming homogenous managers in a firm, with a thinking level $s$ employer, the number of managers $n$ with thinking level $s_m$ is given by $\frac{s}{n} / \frac{\sqrt{s_m}}{\lambda} =  1$. In words, the thinking uses up the manager's time by giving him $\frac{s}{n}$ units of ideas per unit of time. The number of doers, since we have $e = 1$ for all people, is then $s$. 

We then naturally has a hierarchical firm structure where due to the production sequence, the thinker is at the top, the managers are in the middle, and the doers are at the bottom.

<div class="image-single">
    <img src="{{ '/cuties/figs/think_do_2/firm_structure.jpg' | relative_url }}" alt="Firm structure" />
</div>
<p style="text-align: center;"><em>Figure: Hierarchy Structure in a Firm</em></p>

The occupational stratification and wage in equilibrium can be derived similarly in the previous post. Intuitively, since our individuals have homogenous doing skills, the logic of comparative advantage requires those who have relatively the least thinking skills to become doers. People with moderate thinking skills = become managers, and those with relatively high thinking skills specialize in producing ideas. We use $s_1$ and $s_2$ to denote the cutoff values for thinking skills between doers and managers, and between managers and thinkers, respectively.

Equilibrium wages are interesting when `managers` come to the economy. Before diving into wages, it's interesting to consider how the value of one single final product is distributed between the doers, managers and thinkers. Remember that we have three types of goods in the economy: ideas, manuals and final products. Thinkers hire managers and doers who produce manuals and finalize products, respectively. Competitive market essentially requires that the unit price of the *services* provided by managers and doers is all equal in the economy. And the wages earned by managers and doers are equal to the speed of providing their *services*. The figure below illustrates the value distribution of a final product.

<div class="image-single">
    <img src="{{ '/cuties/figs/think_do_2/share_allocation.jpg' | relative_url }}" alt="Value distribution of a final product" />
</div>
<p style="text-align: center;"><em>Figure: Value Distribution of a Final Product</em></p>

It's somewhat surprising to note that the coming of managers drives the wages up, exceeding what they would earn as solo workers. The reason is thinkers need to incentivize people to work as managers for otherwise they would find it more profitable to set up their own firms and work as thinkers. This in turn increase the wages for the doer market where employers heavily compete for the resource of doing.


[^1]: Sharma, K. J., & Bowonder, B. (2004). The making of Boeing 777: A case study in concurrent engineering. *International Journal of Manufacturing Technology and Management*, 6(3–4), 254–264. GPT-5.1 suggested this example.