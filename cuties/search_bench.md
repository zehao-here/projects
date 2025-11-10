---
layout: post-cutie
title:  Search or Bench
permalink: /cuties/search_bench/
produced_at: 10 Nov 2025
---


## Story in One Paragraph
Ideas occasionally come to the great mind, who needs extra hands to execute them. She may look for people whenever the idea comes. Alternatively, she may keep a team around ready all the time.


## Model
Time is continuous, $t\ge 0$. Ideas arrive according to a Poisson process with $\lambda>0$. An idea that is executed delivers a one-off payoff $V>0$ at the (instant of) execution. Execution requires a team of size $L$. The firm can operate under one of two staffing regimes:

- **Flexible (F, search on demand).** For each arrival $\tau_n$, the firm initiates matching. The time until work can start is $T\sim \mathrm{Exp}(\mu)$, independent across idea arrivals, so that $\mathbb{E}[e^{-r T}]=\frac{\mu}{\mu+r}$. Execution is instantaneous once a match is found. The firm pays a one-time matching/search fee $c\ge 0$ per idea (interpreting $c$ as hiring/onboarding and search frictions). No ongoing wage is paid outside matching.

- **Regular (R, bench).** The firm maintains $L$ workers on payroll at all times and pays a wage flow $w$ per worker, i.e., a total burn $wL$ per unit of time. With a staffed bench, ideas are executed immediately upon arrival (no delay, no search fee).

The firm discounts flows at the constant rate $r>0$.

## Analysis

The expected payoff of the firm is the expected present value of exectued ideas minus the cost of search friction or the wage flow, depending on the staffing regime. Let $\Pi_F$ and $\Pi_R$ denote the expected payoff of the flexible and regular regimes, respectively. Then we have

\[
\Pi_F = \frac{\lambda}{r}(\frac{\mu}{\mu+r}V - cL),
\]
and
\[
\Pi_R = \frac{\lambda}{r}V - \frac{wL}{r}.
\]

Note that the regular regime is preferred iff $\Pi_F \leq \Pi_R$, which we can simplify as
\[
(w - \lambda c) L \leq \lambda \left(\frac{r}{\mu+r}V\right),
\]
or equivalently,
\[
w \leq \lambda \left(\frac{r}{\mu+r}\frac{V}{L} + c\right).
\]

