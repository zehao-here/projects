---
layout: post-cutie
title: The Use and Abuse of Evidence
permalink: /cuties/use_evidence/
produced_at: 26 Oct 2025
---

<!-- *Meta writes a list showing how many lines of codes are written by each person. Is that the best possible way to pick out LeCun?* -->

## Model

The environment parallels the uniform-quartic case in Crawford and Sobel (1982)[^1], but we do not discuss communication here.

**Environment.** A principal $P$ needs to choose an action $a \in \mathbb{R}$ for a single project. Good decision needs to be close to the state of the world $\theta \in \Theta = [0,1]$. One agent $A$ observes the realized state and may present evidence to the principal.

**Preferences.** The principal's payoff is $u_P(a,\theta) = -(a-\theta)^2$. Agent $A$ receives $u_{A}(a) = -a^2$; hence $A$ is biased toward actions closer to 0.

**Evidence.** Agent $A$ is endowed with a set of hard-evidence technologies. Each hard-evidence technology is represented by a partition $\mathcal{E}$ of $\Theta$. For any realization $\theta \in e \in \mathcal{E}$, agent $A$ can verifiably disclose the element $e$ to the principal. The set of all partitions $\lbrace \mathcal{E} \rbrace$ and the payoff primitives are common knowledge.


## Analysis

We examine two very simple scenarios here. In both cases, we assume that the realization of $\theta = 0.4$.

**Case 1.** Suppose that the only evidence system available is $\mathcal{E_1} = \lbrace [0, 0.8], (0.8, 1] \rbrace$. Then the statement "$\theta \in [0, 0.8]$" is true, and the implemented action will be $a = 0.4$. This is $P$'s best action.

**Case 2.** Suppose that there are two evidence systems available, $\mathcal{E_1} = \lbrace [0, 0.8], (0.8, 1] \rbrace$ and $\mathcal{E_2} = \lbrace [0, 0.2], (0.2, 0.8], (0.8, 1] \rbrace$. The agent $A$ may still present the evidence to $P$ that $\theta \in [0, 0.8]$, but this in effect this is identical to presenting the evidence that $\theta \in (0.2, 0.8]$. The subtle difference here is that $P$ knows the existence of the second evidence system. If it were true that $\theta \in [0, 0.2]$, then $A$ would for sure present this to $P$, whereas he did not. As a result, $P$ will rationally choose $a = 0.5$ as she believes $\theta \in (0.2, 0.8]$. The new evidence system promises preciser information, but it hurts both $P$ and $A$.


[^1]: Crawford, V. P., & Sobel, J. (1982). Strategic information flow. *Econometrica: Journal of the Econometric Society*, 1431-1451.