---
layout: post-cutie
title: Should Platforms Favor New Contents?
permalink: /cuties/new_contents/
produced_at: 31 Oct 2025
---

## Story in One Paragraph

Platforms like TikTok experience cold start problems for new contents. As a result, algorithms are designed to favor new contents by giving them more exposure to users. However, these algorithms may lead to strategic plays by content creators and thus to a decrease in the quality of new contents.

## Model

The classic Tullock (1980)[^1] model is adapted here to reflect the competition between the new content creators and the existing content creators. Let $q$ denote the quality of the new content. We focus on how the decision of the new content's quality $q$ is determined related to the average quality[^2], which is denoted by $\bar{q} \equiv 1$.

To favor new contents, the platform gives favor to the new content in the Tullock competition. The probability of winning is given by $\frac{\alpha^2 q}{\alpha^2 q+\bar{q}} = \frac{\alpha^2 q}{\alpha^2 q+1}$, where $\alpha \geq 1$ represents the platform's favoritism. The new content creator receives a payoff of $1$ if he wins the competition, and $0$ otherwise. To produce the new content, the new content creator needs to spend a cost of $\frac{1}{c^2}q$ where $c > 1$.

## Analysis

We can derive the optimal quality decision of the new content creator by solving the first order condition, which gives us $q^* = \frac{1}{\alpha} c - \frac{1}{\alpha^2}$.

Consider that $\alpha = 1$ where the platform gives no favor to the new content. The optimal quality decision of the new content creator is $q^* = c - 1$. With $\alpha > 1$, the optimal quality is $\frac{1}{\alpha} c - \frac{1}{\alpha^2}$. We can calculate that

\[
(\frac{1}{\alpha} c - \frac{1}{\alpha^2}) - (c-1) = (\frac{1}{\alpha} - 1)c - (\frac{1}{\alpha}-1)(\frac{1}{\alpha}+1) = (\frac{1}{\alpha}-1)(c - \frac{1}{\alpha} - 1).
\]

As a result, as long as $\alpha$ is large enough, we will find that the quality decision of the new content is actually lower than there is no favor.

[^1]: Tullock, Gordon. 1980. “Efficient Rent Seeking.” In *Towards a Theory of the Rent-Seeking Society*, edited by James Buchanan, Roger Tollison, and Gordon Tullock, 97–112. College Station: Texas A&M Univ. Press.
[^2]: It inevitably means that we do not consider how the quality of the average content is then determined.