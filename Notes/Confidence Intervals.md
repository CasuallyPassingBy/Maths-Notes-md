---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Interval estimation]], [[Ancillary Statistic]]

**Def:** Let $X_1, \dots, X_n$ be a random sample of the density $f(x;\theta)$ and $\tau(\theta)$ be function of $\theta$. Let $T_1(\underline X)$ and $T_2(\underline X)$ be such that $T_1 \le T_2$ and $P(T_1 < \tau(\theta) < T_2) = \gamma$, where $0 < \gamma < 1$ independent of $\theta$. Then to $(T_1, T_2)$ is called a random interval and to a value fo the interval $(t_1, t_2)$ is called the confidence interval or interval of $\gamma$ confidence for $\tau(\theta)$.

**Def:** Let $X_1, \dots, X_n$ be a random sample of the density $f(x;\theta)$. Let $T_1(\underline X)$ be a statistic such that $P(T_1 < \tau(\theta)) = \gamma$; then $T_1$ induces a lower unilateral confidence interval $(t_1(\underline x), \infty)$ with confidence level of $\gamma$. Analogously, if $T_2(\underline X)$ is a statistic such that $P(\tau(\theta) < T_2) = \gamma$; then $T_2$ induces the upper unilateral confidence interval $(-\infty, \tau(\theta))$ with a confidence level of $\gamma$. 

# Pivotal Quantity

**Def**: Let $X_1, \dots, X_n$ be a random sample of the density $f(x; \theta)$. Let $Q=q(X_1, \dots, X_n; \theta)$, meaning $Q$ is a function of the random sample and of $\theta$. If the distribution of $Q$ doesn't depend of $\theta$, then $Q$ is called *pivotal quantity*


**Def:** Let $Q = q(x_1, \dots, x_n;\theta)$ be a pivotal quantity. Then for any $\gamma \in (0, 1)$, exist $q_1$ and $q_2$ that depend on $\gamma$ such that $$P(q_1< Q<q_2) = \gamma$$
if for each sample $(x_1, \dots, x_n)$ such that $$q_1 <q(x_1, \dots, x_n ; \theta) <q_2$$
iff $$t_1(x_1, \dots, x_n) <\tau(\theta) < t_2(x_1, \dots x_n)$$
for functions $t_1$ and $t_2$ that do not depend on $theta$, then $(t_1, t_2)$ is an interval of $\gamma$ confidence for $\tau(\theta)$.
The expected length will be $E[t_2(\underline X) - t_1(\underline X)]$.

**Prop:** Let $f(x)$ be a unimodal density and $F$ be the associated cdf. Let $[a,b]$ be an interval that satisfies $$F(b) - F(a) = 1 - \alpha$$
for $0< \alpha<1$. Then between all the intervals that satisfy the condition above, $[a_0, b_0]$ has the minimum length if $f(a_0) = f(b_0) > 0$, and $a_0 \le x^*\le b_0$, where $x^*$ is the mode of $f(x)$. If additionally $f(x)$ is symmetric, then $a_0 = F^{-1}(\alpha/2)$ and $b_0 = F^{-1}(1 -  \alpha/2)$ 
#### Method for continuous distribution functions
**Prop:** Let $X_1, \dots, X_n$ be a random sample from a population with density of $f(x; \theta)$, such that the corresponding cumulative probability function $F(x; \theta)$ is continuous on $x$. Then $\sum\limits_{i = 1}^n\ln(F(X_i;\theta))$ or alternatively $\prod\limits_{i = 1}^n F(X_i;\theta)$ is a pivotal quantity to estimate $\theta$
#### Method based on sufficient statistics
Sometimes it is difficult to get an exact pivotal quantity, so we use different methods. This method is uses [[Sufficient Statistics]] or estimators of the this functions, like the [[Maximum Likelihood estimators]]

Let $X_1, \dots, X_n$ be a random sample of a population with a density function $f(x; \theta)$, where $\theta \in \Bbb R$ is the true value, and $\Theta \subseteq \Bbb R$ is the parametric space. Let $T(\underline X)$ be a statistic, either a sufficient statistic or maximum likelihood estimator of the parameter in mind. We can choose either or, be we want to facilitate the operations we are going to do to get the confidence interval. We are going to calculate the distribution of $T$.

We need to define two functions $h_1(\theta)$ and $h_2(\theta)$ such that $$\begin{align*}
P(T(\underline X) \le h_1(\theta)) = p_1 \\
P(h_2(\theta) \le T(\underline X)) = p_2
\end{align*}$$
where $p_1$ and $p_2$ are fixed numbers such that $p_1, p_2 >0$ and $p_1+p_2 < 1$. Suppose that $h_1(\theta)$ and $h_2(\theta)$ are increasing functions and $h_1(\theta) < h_2(\theta)$.

Let $t_0$ be the observed value of $T$, obtained by the observed sample $\underline x = (x_1, \dots, x_n)$, meaning $T(\underline x) = t_0$. For any value of $t_0$, we can obtain $v_1=v_1(t_0)$ and $v_2 = v_2(t_0)$ such that $(v_1, v_2)$ be the $(1-p_1-p_2)$ confidence interval for $\theta$.

We have that $h_1(\theta) < t_0 < h_2(\theta)$ iff $v_1 < \theta < v_2$ for any observed sample $\underline x$. By definition we have that $$P(h_1[\theta) < T(\underline X) <h_2(\theta)] = 1-p_1-p_2$$
which is equivalent to $$P[v_1(\underline x)< \theta< v_2(\underline x)] = 1 -p_1-p_2 $$Which establishes that $(v_1, v_2)$ is a $(1-p_1-p_2)$ confidence interval for $\theta$. 