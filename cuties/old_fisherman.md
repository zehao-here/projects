---
layout: post-cutie
title: The Old Man and the Sea
permalink: /cuties/old_fisher/
produced_at: 19 Dec 2025
---

## Story in One Paragraph

The old man has spent his whole life on salty, windswept seas. He is a master of two arts, catching fish and salting them. It warms him to see his sons grown strong enough to share the work. He asks himself what to keep in his own hands and what to leave to them. In the end, he finds himself better off going out to fish if the sea is generous enough with good catch, or when his skill of fishing outshines his skill at salting fish.

## Model

An old fisher man lives near a sea with $n$ sons. His family makes a living by selling fish to the market on the town.

The old man is both excellent at fishing and salting fish. Every day, he catches $s_H$ fish and salts $e_H$ fish. His little sons are relatively less skilled. They can catch $s_L$ fish and salt $e_L$ fish each day for each.

There is a vast sea with two kinds of fish leaving in it, good fish and bad fish. Every time when a fish is caught, it is good with probability $\alpha$. Both the old man and his sons tell immediately and perfectly the type of the fish upon catching. Salted good fish taste so good that the merchants are willing to pay $v_H$ for each. The bad fish are rather tasteless and needs only easy processing, of which the value we normalize to be $v_L \equiv 0$, so they can be ignored in the analysis.

The old man pays his each son a pocket money of $w$ for helping him every day, which we assume negligible in the sense that $w << v_H$. We also assume a large enough $n$ (in the sense that the old fishman is also good at having children), so that the old man can always find enough sons to help him.

## Analysis

By the logic of comparative advantage, the old man chooses between two production schemes: either specializes in fishing or in salting fish, and leaves the other to his sons. 

<div class="image-single">
    <img src="{{ '/cuties/figs/old_fisherman/two_schemes.jpg' | relative_url }}" alt="Production Schemes" />
</div>


Because $w$ is small, the number sons hired by the old man is determined by the amount of fish catched or to be salted. In the first scheme, it is $\alpha s_H = n_1 e_L$, and in the second scheme, it is $n_2 \alpha s_L = e_H$. Write the payoff of the old man in scheme $i$ as $\pi_i$. Then we have

\[
\pi_1 = \alpha s_H v_H - n_1 w = \alpha s_H (v_H - \frac{w}{e_L}),
\]
and
\[
\pi_2 = e_H v_H - n_2 w = e_H (v_H - \frac{w}{\alpha s_L}).
\]

The first scheme is preferred iff $\pi_1 \geq \pi_2$, which we can simplify as

\[
\alpha \geq \frac{e_H}{s_H} \frac{v_H - \frac{w}{\alpha s_L}}{v_H - \frac{w}{e_L}} \approx \frac{e_H}{s_H}.
\]

Suppose that a supper cool fish-salting container is invented by the old man, he may find it profitable to switch to the second scheme.