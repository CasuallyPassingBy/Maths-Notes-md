---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measures]], [[Measure Spaces and Measurable Spaces]]

**Def:** Let $(X, {\scr A})$ be a measurable space. A subset $X$ is *universally measurable* with respect to $(X, {\scr A})$ if it is $\mu$-measurable for every finite measure $\mu$ on $(X, {\scr A})$. Let $\scr A_*$ be the family of all universally measurable subsets of $X$. 

**Obs:** Then ${\scr A}_* =\bigcap_\mu {\scr A}_\mu$, where $\mu$ ranges over the family of finite measures on $(X, {\scr A})$; hence $\scr A_*$ is a $\sigma$-algebra. It is easy to check that for each finite measure $\mu$ on $(X, {\scr A})$ there is a unique measure on $(X, {\scr A}_*)$ that agrees on $\scr A$ with $\mu$. 

**Prop:** Let $(X, {\scr A})$ be a measurable space. 
- $({\scr A}_*)_* = \scr A_*$.
- If $\mu$ is a finite measure on $(X,{\scr A})$, then $({\scr A}_\mu)_* = \scr A_\mu$. 

**Prop:** Let $(X, {\scr A})$ be a measurable space.
- A function $f:X\to \overline{\Bbb R}$ is $\scr A_*$-measurable iff for each finite measure $\mu$ on $(X, {\scr A})$ there are $\scr A$-measurable functions $f_0, f_1: X\to \overline{\Bbb R}$ that satisfy $f_0 \le f \le f_1$ everywhere on $X$ and are equal to one another $\mu$-almost everywhere on $X$.
- If $f:X \to \overline{\Bbb R}$ is $\scr A_*$-measurable and if the functions $f_0$ and $f_1$ above are independent of the chosen metric, then $f$ is $\scr A$-measurable. 
