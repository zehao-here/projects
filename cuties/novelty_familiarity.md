---
layout: post-cutie
title: Beep Beep I'm a Sheep ... but R&B
permalink: /cuties/novelty_familiarity/
produced_at: 10 Nov 2025
---


## Story in One Paragraph

AI models like Suno has greatly changed the landscape of music production. More than often, however, I observe that people offer only sparse applause for purely AI-generated pieces, yet they readily praise AI rearrangements of well-known songs. AI releases creativity, while it leans more on a bedrock of familiarity.


## Model

Let's talk about music!

There is a unit mass of audience who in general love novel songs. However, it takes efforts to appreciate novelty, and less familiarity generates more cognitive efforts to appreciate. Formally, we represent the audience's utilities as a function of $u_a = tx - \frac{1}{2}\frac{1}{\gamma}x^2$. The meanings of the parameters are as follows: $t >0 $ captures different tastes for novelty, $x$ denotes the amount of novelty as a consumption good, and $\gamma > 0$ captures the familiarity of the music produced. The audience distributes uniformly over $t \in [0,1]$.

Two music producers, $1$ and $2$, live in the economy who writes different types of songs. Producer 1 enjoys creating niche songs with familiarity $\gamma_1$, while Producer 2 focuses on writing mainstream songs with familiarity $\gamma_2$. We assume that $\gamma_1 < \gamma_2$. 

The two producers share the same production technology which is characterized by a cost function of $c(x, \gamma) = \frac{1}{2}\lambda \gamma x^2$. In words, it is always more difficult to produce a more novel song with higher familiarity. Both enjoy a utility of $1$ for obtaining an extra unit of audience. That is, the utility of producers is $u_p(x, \gamma) = D - c(x, \gamma)$ where $D$ is the audience's demand for the music produced. Each audience choose whatever producer offering the higher utility. 


## Analysis

Our model shares some spirits with the classic Hotelling (1929) model.[^1] We assume interior solution here.

Given the familiarity level $\gamma$, the producer's optimal choice of novelty follows from the "MR = MC" reasoning. 


[^1]: Hotelling, H. (1929). Stability in Competition. *The Economic Journal*, 39(153), 41–57.