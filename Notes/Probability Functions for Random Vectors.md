---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Probability Functions for Random Variables]], [[Random Vectors]]

# Joint Probability Distribution

The function of a two dimensional discrete random vector $(X, Y)$, where the possible values for $X$, are $x_1, x_2, \dots$ and the possible values for $Y$ are $y_1, y_2, \dots$, the function $f:\Bbb R^2 \to [0,1]$ defined as

$$ f(x,y) = \begin{cases} P(X = x, Y= y) &(x,y) \in \{x_1, x_2, \dots\} \times \{y_1, y_2,\dots\} \\ 0 & \text{otherwise} \end{cases} $$

We usually use refer to it as $f_{X,Y}$ since we know which random variables we are taking about, and this is the joint probability mass function of two random variables.

Each joint probability mass function of two random variables, must satisfy the following properties:

- $f(x,y) \ge 0$
- $\sum\limits_{x,y} f(x,y) = 1$

Let $A$ and $B$ be Borel sets, then the probability that $(X \in A) \cap(Y \in B)$ is given by the formula:

$$ P(X\in A, Y \in B) = \sum_{x \in A} \sum_{y \in B} f_{X,Y}(x,y) $$

Let $(X, Y)$ be a continuous random vector with a distribution function $F$. We say that $(X, Y)$ is absolutely continuous if there's a nonnegative integrable function $f:\Bbb R^2\to [0,\infty)$, such that for all $(x, y)\in \Bbb R^2$, it follows that
$$
	F(x, y) = \int_{-\infty}^x\int_{-\infty}^yf(u, v)\, dv\, du
$$

All pdf $f$ mus satisfy the following characteristics:

- $f(x,y) \ge 0$
- $\int_{\Bbb R}\int_{\Bbb R} f(u,v) \,dv\, du = 1$

Given $a<b$ and $c < d$, we can calculate the probability of $(a < X<b) \cap (c< Y<d)$, it is calculated by

$$ P(a<X<b,c<Y<d) = \int_{a}^b\int_{c}^d f(u,v) \,dv\, du $$

---

# Joint Cumulative Distribution Function

The cdf of the vector $(X,Y)$ is denoted as $F: \Bbb R^2 \to [0,1]$, it is defined as

$$ F(x,y) = P(X \le x, Y\le y) $$

The cdf $F$ of a random vector $(X,Y)$ satisfies the following properties:

- $\lim\limits_{x \to \infty} \lim\limits_{y \to \infty} F(x,y) = 1$
    
- $\lim\limits_{x \to -\infty} F(x, y) = \lim\limits_{y \to -\infty} F(x,y) =0$
    
- $F(x,y)$ is right continuous on each variable
    
- $F(x,y)$ is a monotonous nondecreasing function on each variable
    
- For any number $a<b$ and $c <d$ , it follows that
    
    $$ F(b,d) -F(a,d)-F(b,c) + F(a,b)= P(a<X\le b, c <Y\le d) \ge0 $$
    
We say that a function $F:\Bbb R^2 \to [0,1]$, not necesarily defined on terms of a random vector, is a conjoined probability distribution function if it follows the five properties above. 

We define the cdf of random vector $(X_1,\dots, X_n)$ as the function $F:\Bbb R^n \to [0,1]$ given by

$$ F(x_1, \dots, x_n) = P(X_1 \le x_1, \dots, X_n\le x_n) $$

Let $F:\Bbb R^n \to [0,1]$ be a distribution function if it follows the first four properties, and additionally, for any numbers $a_1 < b_1, a_2 < b_2, \dots a_n < b_n$, 
$$
\sum_{x_i \in \{a_i, b_i\}} (-1)^{\#a} F(x_1, \dots, x_n) \ge0
$$
where $\#a$ is the number of times that the variables $x_i$ takes the value $a_i$ in the evaluation of $F$.

Let $F:\Bbb R^n \to [0, 1]$ be distribution function. Then there's a probability space $(\Omega, {\scr F}, P)$ and a random variable such that $F$ is the its distribution function.

### From the pdf/pmf to cdf
If we have the cdf $f(x,y)$ (in the continuous case) we can find the cdf $F(x,y)$, we calculate it as

$$ F(x,y) = \int_{-\infty}^x\int_{-\infty}^y f(u,v) \,dv\, du $$

if we have the pmf $f(x,y)$ (in the discrete case) we can find the cdf $F(x,y)$, we calculate it as

$$ F(x,y) = \sum_{u \le x} \sum_{v \le y} f(x,y) $$

### From the cdf to pdf/pmf

In the continuous case, given the cdf $F(x,y)$ we can calculate the pdf $f(x,y)$ as

$$ f(x,y) = \frac{\partial^2}{\partial x \partial y} F(x,y) $$

In the discrete case, given the cdf $F(x,y)$ we can calculate the cdf $f(x,y)$ as

$$ f(x,y) = F(x,y)-F(x-, y)-F(x,y-)+F(x-,y-) $$