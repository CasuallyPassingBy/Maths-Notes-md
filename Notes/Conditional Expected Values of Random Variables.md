---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Conditional Distribution Functions]], [[Expected Value of Random Variables]], [[Rings and Algebras of Sets]]

# With Respect to a $\sigma$-algebra

Let $X$ be a random variable with finite expected value, and let $\scr G$ a sub-$\sigma$-algebra on $\scr F$. The expected value of $X$ given $\scr G$, is random variable denoted as $\Bbb E(X \mid \mathscr G)$, that satisfies the following properties:
- it is $\scr G$ measurable
- Has finite expected value
- For any event $G$ in $\scr G$ $$\Bbb E[\Bbb E(X \mid \mathscr G) \cdot 1_G] = \Bbb E[X \cdot 1_G]$$
Let $X$ have finite expected value, and $A$ and $B$ be events such that $0 <\Bbb P(A)< 1$. Then:
- $\Bbb E(X \mid \{\varnothing, \Omega\}) = \Bbb E[X]$
- $\Bbb E(1_A \mid \{\varnothing, \Omega\}) = \Bbb P(A)$
- $\Bbb E(1_A \mid \{\varnothing,B, \Omega \setminus B ,\Omega\}) = \Bbb P(A\mid B)\cdot 1_B + \Bbb P(A\mid \Omega\setminus B) \cdot 1_{\Omega\setminus B}$ 

We can generalise this last result as:
Let $B_1, \dots, B_n$ a partition of $\Omega$ and each of the elements has a strictly positive probability. Then for any event $A$, it satisfies $$\Bbb E(1_A \mid \sigma(\{B_1, \dots, B_n \})) = \sum_{i = 1}^n \Bbb P(A \mid B_i)\cdot 1_{B_i} $$

**Prop:** Let $X$ and $Y$ be random variables with finite expected value and $c$ a constant. Them 
- if $X\ge 0$, then $\Bbb E(X \mid \mathscr G) \ge 0$
- $\Bbb E(cX + Y \mid \mathscr G) = c\Bbb E(X \mid \mathscr G) + \Bbb E(Y \mid \mathscr G)$ 
- If $X \le Y$, then $\Bbb E(X \mid \mathscr G) \le \Bbb E(Y \mid \mathscr G)$ 
- $\Bbb E[\Bbb E(X \mid \mathscr G)] = \Bbb E[X]$
- If $X$ is $\mathscr G$ measurable, then $\Bbb E(X \mid \mathscr G) = X$, $a.e.$. In particular $\Bbb E(c \mid \mathscr G) = c$ 
- If $\mathscr G_1 \subseteq \mathscr G_2$, then $$\Bbb E(\Bbb E(X \mid \mathscr G_1)\mid \mathscr G_2) =  \Bbb E(\Bbb E(X \mid \mathscr G_2) \mid \mathscr G_1)  = \Bbb E(X \mid \mathscr G_1)$$
## Conditional Variance

Let $X$ with a second moment that is finite, and $\mathscr G$ be a sub-$\sigma$-algebra of $\mathscr F$. The conditional variance of $X$ given $\mathscr G$, denoted as $\text{Var}(X \mid \mathscr G)$, it is defined as the random variable
$$\text{Var}(X \mid \mathscr G) = \Bbb E[(X - \Bbb E(X \mid \mathscr G))² \mid \mathscr G] $$
**Prop:** Let $X$ and $Y$ be random variables with finite variance, and $c$ be a constant. Then:
- $\text{Var}(X \mid \mathscr G) \ge 0$
- $\text{Var}(c \mid \mathscr G) = 0$
- $\text{Var}(cX \mid \mathscr G) = c^2 \text{Var}(X \mid \mathscr G)$
- $\text{Var}(X+c \mid \mathscr G) = \text{Var}(X \mid \mathscr G)$ 
- In general $\text{Var}(X+Y \mid \mathscr G)\ne \text{Var}(X \mid \mathscr G)+\text{Var}(Y \mid \mathscr G)$
- $\text{Var}(X \mid \mathscr G) = \Bbb E(X^2 \mid \mathscr G) - E^2(X \mid \mathscr G)$
- $\text{Var}(X ) = \Bbb E[\text{Var}(X \mid \mathscr G)]+ \text{Var}(\Bbb E[X \mid \mathscr G])$  

# With Respect to Random Variables

Let $(X, Y)$ be a random vector with a distribution function $F_{X, Y}(x, y)$ and let $y$ be a value such that $f_Y(y)\ne 0$. If $X$ has finite expected value, then we define
$$
\Bbb E[X\mid Y =y] = \int_\Bbb R x \, dF_{X\mid Y}(x\mid y)
$$


Let $(X, Y)$ be a continuous random vector with a density function $f_{X,Y} (x, y)$ and let $y$ be such that $f_Y(y)\ne 0$. The conditional expected value of $X$ given $Y=y$, is the expected value of the conditional density function $f_{X\mid Y}(x\mid y)$, when it exits, i.e.
$$
\Bbb E[X\mid Y= y] = \int_{\Bbb R}xf_{X\mid Y}(x\mid y)\, dx
$$
We can see that 
$$
\Bbb E[X] = \int_{\Bbb R} \Bbb E[X\mid Y=y] f_Y(y)\, dy
$$
and similarly for the discrete being 
$$
	\Bbb E[X\mid Y= y] = \sum_{x}xf_{X\mid Y}(x\mid y)
$$
and 
$$
\Bbb E[X] = \sum_{y} \Bbb E[X\mid Y=y] f_Y(y)
$$