---
layout: post-cutie
title: Should Platforms Favor New Contents?
permalink: /cuties/new_contents/
produced_at: 31 Oct 2025
---

*Update: I have incorporated the equilibrium effect into the model. (Nov 4, 2025)*

## Story in One Paragraph

Platforms like TikTok experience cold start problems for new contents. As a result, algorithms are designed to favor new contents by giving them more exposure to users. However, these algorithms may lead to strategic plays by content creators and thus to a decrease in the quality of new contents.

## Model

The classic Tullock (1980)[^1] model is adapted here to reflect the competition between the new and the existing content creators, which we reduce to a single __average__ content creator. Let $q$ denote the quality of the new content. The average quality of the contents on the platform is denoted by $\bar{q}$.

To favor new contents, the platform gives favor to the new content in the Tullock competition. The probability of winning is given by $\frac{\alpha^2 q}{\alpha^2 q+\bar{q}} = \frac{\alpha^2 q}{\alpha^2 q+1}$, where $\alpha \geq 1$ represents the platform's favoritism. The new content creator receives a payoff of $1$ if he wins the competition, and $0$ otherwise. To produce the new content, the new content creator needs to spend a cost of $\frac{1}{c^2}q$ where $c > 1$.

## Analysis

Let's first consider the case where the platform gives no favor to the new content, i.e., $\alpha = 1$. We can derive the optimal quality decision of the new content creator by solving the first order condition, which gives us the equation $q^* = c\sqrt{\bar{q}} - \bar{q}$.

In the symmetric equilibrium, the average quality $\bar{q}$ is equal to the optimal quality of the new content $q^*$. Substituting $\bar{q}$ with $q^*$ in the first order condition, we get $q^* = \frac{c^2}{4}$.

Now suppose that $\alpha > 1$. Given the current average quality $\bar{q}$, the new content creator's optimal quality decision (which we denote by $q_{\alpha}^{\ast}$) can be calculated again by attacking the first order condition, which gives us the equation $q_{\alpha}^{\ast} = \frac{1}{\alpha^2}\left(\alpha c\sqrt{\bar{q}} - \bar{q}\right)$.

Now we compare the optimal choice of the new content and the average quality. It is found that 
\[
 q_{\alpha}^{\ast} - \bar{q} = \frac{1}{\alpha^2}\left(\alpha c\sqrt{\bar{q}} - \bar{q}\right) - \bar{q} = \frac{1}{\alpha^2}\left(\alpha c\sqrt{\bar{q}} - (1+\alpha^2) \bar{q}\right) = \frac{\bar{q}}{\alpha}(c - (\frac{1}{\alpha}+\alpha)\sqrt{\bar{q}})
\]

Thus, as long as $\bar{q} \geq \frac{c^2}{(\alpha + \frac{1}{\alpha})^2}$, the new content creator will choose a lower quality than the average quality. Under this new-content-favor polity, the quality of the contents will then converge to $\frac{c^2}{(\alpha + \frac{1}{\alpha})^2}$.

Finally, notice that $q_{\alpha}^{\ast} = \frac{c^2}{(\alpha + \frac{1}{\alpha})^2} \leq \frac{c^2}{4} = q^{\ast}$ and the inequality is strict if $\alpha > 1$. The platform's favoritism will possibly lead to a decrease in the quality of the contents.


[^1]: Tullock, Gordon. 1980. “Efficient Rent Seeking.” In *Towards a Theory of the Rent-Seeking Society*, edited by James Buchanan, Roger Tollison, and Gordon Tullock, 97–112. College Station: Texas A&M Univ. Press.