---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Interval estimation]]

**Def**: A statistical hypothesis is an assertion about the distribution of one or more random variables. A hypothesis specifies completely the distribution is called *simple hypothesis*. A hypothesis that is not simple it is called a *composite hypothesis*. 

**Def:** A *hypothesis test* is a decision rule through which, and base on the sample, we can determine to accept or deny the null hypothesis that we are considering.

**Def:** The región $\mathcal C$ that leads us to reject the null hypothesis is called the *critical region* or *rejection region*.

Some notation that is going to be useful :
- $\gamma$ usually represent s hypothesis test
- $\mathcal C$ or $\mathcal C_\gamma$ it refers to the critical region related to the test $\gamma$
- $\Theta$ is the parametric space
- $\Theta_0$ is the parametric space that is consistent with the null hypothesis $H_0$
- $\Theta_1$ is the parametric space that is consistent with the alternative hypothesis $H_1$

# Types and Error Sizes

|                  | $H_0$ is true         | $H_0$ is false         |
| ---------------- | --------------------- | ---------------------- |
| Reject $H_0$     | Error type $\text{I}$ | Right choice           |
| Not Reject $H_0$ | Right choice          | Error type $\text{II}$ |

We also define the *size of the errors* as $$\alpha =P(\text{Error type I}) = P(\text{reject }H_0 \mid H_0 \text{ true})$$and $$
\begin{align*}
	\beta &= P(\text{Error type II}) = P(\text{Not Rejecting }H_0 \mid H_1 \text{ true}) \\
	&= P(\text{Error type II}) = P(\text{Not Rejecting }H_0 \mid H_0 \text{ false})
\end{align*}
$$
# The Power function

**Def:** The *power of of test* $\gamma$ is given by $$\pi_\gamma(\theta) = P(\text{Reject } H_0 \mid \theta) = P(\underline X \in \mathcal C\mid \theta)$$
The *ideal power function* is $0$ for all $\theta \in \Theta_0$ (the null hypothesis) and $1$ for $\theta \in \Theta_1$ (the alternative hypothesis). Meaning that $$P(\text{Reject }H_0 \mid \theta) = \begin{cases}
0 & \theta \in \Theta_0 \\
1 & \theta \in \Theta_1 \\
\end{cases}$$

**Def:** Let $\gamma$ be a hypothesis test of $H_0 : \theta \in \Theta_0$ against $H_1: \theta \in \Theta_1$. The *size of the test* is defined: $$\max_{\theta \in \Theta_0} \pi_\gamma(\theta)$$meaning, the maximum of the power function when $H_0$ is true

There are different types of hypothesis test
- [[Statistical Test for Simple Hypotheses]]
- [[Uniformly Most Powerful Tests]]
- [[Generalised Likelihood Ratio]]
-  [[P-value and Statistical Significance Test]]