---
layout: post-cutie
title: The Bumpy Proof
permalink: /cuties/bumpy_proof/
produced_at: 03 Jan 2026
---

---

## Story in One Paragraph

A hard math problem rarely feels uniformly hard in every step. The beginning is full of fog: what route to take, which lemma matters, where the hidden structure is. Later, once the right path is found, the work becomes more mechanical—algebra, bookkeeping, and checking edge cases. However, it still takes effort to deal with these nasty details. I model this and highlight the merit of cooperation. The story has changed its appearance, but the core is still the previous one about comparative advantage.

## Model

**Players and skills.** There are two solvers, $A$ and $B$, with innate thinking skills $s_A > s_B > 0$.

**Production.** Value comes from solving problems. To what extent a problem is solved is represented by a *completeness index* $x \in [0,1]$, where $x=0$ means a blank page, and $x=1$ means a complete correct solution. 

The difficulty to dealing with the problem varies at different completeness levels, which is captured by *bumpiness* as a function $\phi(x)$. It is assumed that $\phi(x)$ is positive, a.e. continuous, decreasing (earlier steps are bumpier), and concave. Bumpiness affects the *instantaneous time* required to make progress, which is given by $\frac{\phi(x)}{s} + h$, where $h>0$ is constant.

A completed solution is valued by the total bumpiness $\int_0^1 \phi(x) dx \equiv v_\phi$.

**Work modes.** Two working modes are available.(i) Separate solving. Each solver completes full solutions alone. (ii) Cooperation. The two players may split the whole problem into a number of sub-problems (a partition of $[0,1]$ into a number of sub-intervals with positive measures), and assign each sub-problem to one of them. The problem is perfectly divisible. No costs are present in coordination or communication.

The problem solvers seek to maximize the rate of value creation per unit of time.


## Analysis

### 1) Separate production

If solver $i\in\{A,B\}$ works alone, the time to finish one full problem is
\[
T_i = \int_0^1\Big(\frac{\phi(x)}{s_i}+h\Big)\,dx
= \frac{v_\phi}{s_i}+h.
\]
So the value creation rate is
\[
R_i^{\text{sep}}=\frac{v_\phi}{T_i}.
\]
Total value creation rate under separate work:
\[
R^{\text{sep}}=\frac{v_\phi}{T_A}+\frac{v_\phi}{T_B} = v_\phi (\frac{1}{T_A} + \frac{1}{T_B}).
\]

### 2) Cooperation

One can imagine that the optimal strategy should take this form: splitting the problem into only two parts and assigning the more difficult part (closer to 0) to the higher-skill solver. That is, they choose a cutoff completeness level $\tilde x \in [0,1]$ such that $A$ does $[0,\tilde x]$ and $B$ does $[\tilde x,1]$.

Given cutoff $\tilde x$, the time to complete the problem is
\[
t_A(\tilde x)=\int_0^{\tilde x}\Big(\frac{\phi(x)}{s_A}+h\Big)\,dx
=\frac{\Phi(\tilde x)}{s_A}+h\tilde x,
\]
\[
t_B(\tilde x)=\int_{\tilde x}^{1}\Big(\frac{\phi(x)}{s_B}+h\Big)\,dx
=\frac{v_\phi-\Phi(\tilde x)}{s_B}+h(1-\tilde x).
\]
Let us ignore the starting stage of dealing with the very first problem. In steady state, the two players employ a pipeline production style and split the problem in at a suitable cutoff level $\tilde{x}$ such that $t_A(\tilde{x}) = t_B(\tilde{x}) = t^\star$, since otherwise one player will be idle waiting for the other.


Then cooperative value creation rate is
\[
R^{\text{coop}}=\frac{v_\phi}{t^\star}.
\]


### 3) Cooperation is more efficient than separate work

We wanted to show
\[
R^{\text{coop}} \ge R^{\text{sep}}
\quad\Longleftrightarrow\quad
\frac{v_\phi}{t^\star}\ge \frac{v_\phi}{T_A}+\frac{v_\phi}{T_B}
\quad\Longleftrightarrow\quad
\frac{1}{t^\star}\ge \frac{1}{T_A}+\frac{1}{T_B}.
\]
The inequalities above actually hold, while the formal derivations can be a bit messy. Readers are invited to check the details in the appendix.

 Intuitively, applying the logic of comparative advantage, it is more efficient to let the higher-skill solver handle the more difficult part and the lower-skill solver takeover the “fixed time cost” part in which the constant term $h$ holds more weight. 



---

## Appendix

**Key Inequality.**
A key inequality is that, for all $x\in[0,1]$, we have $\Phi(x)\ge x\,v_\phi$. (Because $\phi$ is decreasing, the average bumpiness in the interval $[0,x]$, i.e., $\frac{\Phi(x)}{x}$, is at least $v_\phi$.)


**(I) Express $t^\ast$ in terms of $x^\ast$.**
From $t^\ast=t_A(x^\ast)$ and $t^\ast=t_B(x^\ast)$,
\[
s_A t^\ast=\Phi^\ast + h s_A x^\ast,\qquad
s_B t^\ast=v_\phi-\Phi^\ast + h s_B(1-x^\ast).
\]
Adding yields
\[
\boxed{\ 
t^\ast=\frac{v_\phi+h\big(s_A x^\ast+s_B(1-x^\ast)\big)}{s_A+s_B}.
\ }
\tag{A}
\]
Note $\partial t^\ast/\partial x^\ast = \frac{h(s_A-s_B)}{s_A+s_B}>0$, so $t^\ast$ is increasing in $x^\ast$.

**(II) Linear link between $\Phi^\ast$ and $x^\ast$.**
Equalization $t_A(x^\ast)=t_B(x^\ast)$ gives
\[
\frac{\Phi^\ast}{s_A}+h x^\ast=\frac{v_\phi-\Phi^\ast}{s_B}+h(1-x^\ast).
\]
Rearranging,
\[
\Phi^\ast\Big(\frac1{s_A}+\frac1{s_B}\Big)=\frac{v_\phi}{s_B}+h(1-2x^\ast).
\]
Let
\[
\theta:=\frac{s_A}{s_A+s_B},\qquad \kappa:=\frac{s_A s_B}{s_A+s_B}.
\]
Since $\big(\frac1{s_A}+\frac1{s_B}\big)^{-1}=\kappa$, we get
\[
\boxed{\ \Phi^\ast=\theta v_\phi+\kappa h(1-2x^\ast).\ }
\tag{B}
\]

**(III) Bounding $x^\ast$.**
Combine $\Phi^\ast\ge x^\ast v_\phi$ with (B):
\[
x^\ast v_\phi \le \theta v_\phi+\kappa h(1-2x^\ast).
\]
Solve for $x^\ast$:
\[
x^\ast(v_\phi+2\kappa h)\le \theta v_\phi+\kappa h
\quad\Rightarrow\quad
\boxed{\ x^\ast\le \bar x:=\frac{\theta v_\phi+\kappa h}{v_\phi+2\kappa h}.\ }
\tag{C}
\]

**(IV) Bounding $t^\ast$ and comparing to separate work.**
Recall that
\[
T_A=h+\frac{v_\phi}{s_A},\qquad T_B=h+\frac{v_\phi}{s_B}.
\]
Since $t^\ast$ is increasing in $x^\ast$ by (A), and $x^\ast\le \bar x$ by (C), we get
\[
t^\ast \le \frac{v_\phi+h\big(s_A \bar x+s_B(1-\bar x)\big)}{s_A+s_B} = \frac{T_A T_B}{T_A+T_B}，
\]
where the last equality is obtained by plugging in the expression of $\bar x$.

Taking reciprocals (all positive), it is established that
\[
\frac1{t^\ast}\ge \frac1{T_A}+\frac1{T_B}. 
\]
