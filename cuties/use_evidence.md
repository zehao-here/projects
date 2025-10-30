---
layout: post-cutie
title: The Use and Abuse of Evidence
permalink: /cuties/use_evidence/
produced_at: 26 Oct 2025
---

<!-- *Meta writes a list showing how many lines of codes are written by each person. Is that the best possible way to pick out LeCun?* -->

## Model

The environment may look similar to the uniform-quartic case in Crawford and Sobel (1982)[^1], but we do not discuss communication here.

**Environment.** A principal $P$ needs to choose an action $a \in \mathbb{R}$ for a single project. Good decision needs to be close to the state of the world $\theta \in \Theta = [0,1]$. One agent $A$ observes the realized state and may present evidence to the principal.

**Preferences.** The principal's payoff is $u_P(a,\theta) = -(a-\theta)^2$. Agent $A$ receives $u_{A}(a) = -a^2$; hence $A$ is biased toward actions closer to 0. For a real world justification, you can think of the scenario where the company would like to make an appropriate amount of investment, while the manager always prefers to invest more.

**Evidence.** Agent $A$ is endowed with a set of hard-evidence technologies. Each hard-evidence technology is represented by a partition $E$ of $\Theta$. For any realization $\theta \in e \in E$, agent $A$ can verifiably disclose the element $e$ to the principal. The set of all evidence systems $\lbrace E \rbrace$ and the payoff structures are common knowledge.


## Analysis

We examine two very simple scenarios here. In both cases, we assume that the realization of $\theta = 0.4$.

**Case 1.** Suppose that the only evidence system available is $E_1 = \lbrace [0, 0.8], (0.8, 1] \rbrace$. Then the statement "$\theta \in [0, 0.8]$" is true, and the implemented action will be $a = 0.4$. This is $P$'s best action.

**Case 2.** Suppose that there are two evidence systems available, $E_1 = \lbrace [0, 0.8], (0.8, 1] \rbrace$ and $E_2 = \lbrace [0, 0.2], (0.2, 0.8], (0.8, 1] \rbrace$. This can be understood as some sort of technological progress: previously, only less powerful analytical tools were available, but now more precise measures of the state of the world are possible. Alternatively, tech progress offers us with some new measures of the state of the world.

The biased agent always would like to induce a low action. Since $\theta = 0.4$, the agent $A$ may still present the evidence to $P$ saying "$\theta \in [0, 0.8]$". However, the older evidence system actually loses its use here; actually this is identical to presenting the evidence that "$\theta \in (0.2, 0.8]$". The subtle difference here is that $P$ knows the existence of the second evidence system. If it were true that $\theta \in [0, 0.2]$, then $A$ would for sure present this to $P$, whereas he did not. As a result, $P$ rationally understands that $\theta \in (0.2, 0.8]$ and chooses $a = 0.5$ as a consequence. The new evidence system promises preciser information, but it hurts both $P$ and $A$ in this case.



[^1]: Crawford, V. P., & Sobel, J. (1982). Strategic information transmission. *Econometrica: Journal of the Econometric Society*, 1431-1451.
