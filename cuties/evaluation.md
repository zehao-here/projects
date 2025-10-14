---
layout: post-cutie
title: Sine of the Students (Evaluation Design of Two Courses)
permalink: /cuties/evaluation/
---

# Sine of the Students

*Zehao Zhang*

## Model

### Students

There are two students, $x$ and $y$, who both attend two courses denoted by $j \in \lbrace1,2\rbrace$. Each student chooses an intensity $r_i \in [0,1]$ and an angle $\varphi_i \in [0, \tfrac{\pi}{2}]$. Due to an energy constraint, efforts are parameterized by the unit quarter-circle:

\[
(e_{i1}, e_{i2}) = r_i (\cos \varphi_i, \sin \varphi_i), \qquad e_{i1}^2 + e_{i2}^2 \le 1.
\]

The outcomes in the courses are normalized to equal effort, so $y_{ij} = e_{ij}$. Student $x$ only cares about reach on the $x$-axis, while student $y$ only cares about reach on the $y$-axis. Both students try their best to avoid triggering the policy penalty defined below.

Without loss of generality, assume the budget binds in the relevant cases ($r_i = 1$).

### Lecturers

There are two lecturers, one for each course $j \in \lbrace1,2\rbrace$. The outcome gap across students is $\Delta_j \equiv \max_{i \in \lbrace x,y \rbrace} y_{ij} - \min_{i \in \lbrace x,y \rbrace} y_{ij}$. A lecturer becomes very upset if she observes a large gap $k \in (0,1)$ between the highest and lowest outcomes. Formally, the lecturer's utility is $0$ if $\Delta_j < k$ and $-\infty$ otherwise.

### Director

The director cares about lecturers' welfare and employs a minimal policy to minimize distortions to students' efforts. To ensure the outcome gap is not too large, she requires each student to reach at least a minimum outcome in each course. Given $c_j \ge 0$, if any student $i$ attains $y_{ij} < c_j$ in course $j$, then that student's utility is $-\infty$.

## Analysis

### Pre-AI Age

Students $x$ and $y$ prefer outcomes $(1, 0)$ and $(0, 1)$, respectively, but such allocations greatly upset the lecturers. Given the properties of the setup, a minimal policy satisfying the lecturers' requirement can be identified, as illustrated below.

### Post-AI Age

Suppose AI greatly improves productivity in course 1, making efforts on the $x$-axis more efficient. Blue denotes efforts and outcomes prior to AI. If the director only raises the minimum requirement $c_1$ on the $x$-axis, AI benefits student $x$ but harms student $y$. Student $y$ has no choice but to allocate less effort to course 2, which he prefers. The director can instead raise $c_2$ to balance the outcomes.

<div class="image-row">
  <img src="{{ '/cuties/figs/evaluation/fig1.jpg' | relative_url }}" alt="Pre-AI" />
  <img src="{{ '/cuties/figs/evaluation/fig2.jpg' | relative_url }}" alt="Post-AI" />
</div>

*Figure: Policies and outcomes in the pre- and post-AI scenarios.*

