---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Confidence Intervals]], [[Normal Distribution]], [[Chi-squared Distribution]], [[Student's t-distribution]], [[F-distribution]]

We need a some properties of the normal distribution, and adjacent distributions

- If $X \sim N(0, 1)$ then $X^2 \sim \chi^2(1)$ 
- If $X_1, \dots, X_n$ be independent random variables such that for all $j \in \{1, \dots, n\}$, $X_j \sim \chi^2(m_j)$, then $$\sum_{j = 1}^n X_j \sim \chi^2\left(\sum_{j = 1}^n m_j\right) $$
- If $X_1, \dots, X_n$ be independent random variables such that for all $j \in \{1, \dots, n\}$, $X_j \sim N(\mu, \sigma^2)$: then $$\sum_{j = 1}^n \frac{(X_j - \mu)^2}{\sigma^2} \sim \chi^2(n) $$
- If $X_1, \dots, X_n$ be a random sample of a population $N(\mu, \sigma^2)$, then $$\frac{n-1}{\sigma^2}S^2 \sim \chi^2(n-1)$$
- If $X$ and $Y$ are independent random variables such that $X \sim N(0,1)$ and $Y \sim \chi^2(k)$, then $$\frac{X}{\sqrt{Y/k}}\sim t(k)$$
- If $X_1, \dots, X_n$ be a random sample of a population $N(\mu, \sigma^2)$, then $$\frac{\overline X - \mu}{S/\sqrt n} \sim t(n-1)$$
- If $U$ and $V$ are independent random variables such that $U \sim \chi^2(n)$ and $V \sim \chi^2(m)$, then $$\frac{U/n}{V/m} \sim F(n, m)$$
### Intervals for the mean
#### Where $\sigma^2$ is known
Let $X_1, \dots, X_n$ be a random sample of a population with distribution $N(\mu, \sigma^2)$, where $\sigma^2$ is known. Then we know that $\overline X \sim N(\mu, \sigma^2/n)$, Then $$Q= \frac{\overline X - \mu}{\sigma/\sqrt n} \sim N(0, 1)$$
$Q$ is a pivotal quantity. 
For the confidence interval we consider the quantiles $z_{\alpha/2}$ being that $P(Q \le z_{\alpha/2}) = \alpha/2$, and $z_{1-\alpha/2}$, such that $P(Q \le z_{1-\alpha/2}) = 1-\alpha/2$. Then we begin with $$P(z_{\alpha/2} \le Q \le z_{1-\alpha/2}) = 1-\alpha $$
We would make some algebraic moves, and using the symmetry of the normal; and get that equivalently that $$P\left(\overline X - z_{1-\alpha/2} \frac{\sigma}{\sqrt n} < \mu <\overline X + z_{1-\alpha/2} \frac{\sigma}{\sqrt n} \right) = 1-\alpha$$
We get the $(1-\alpha)$ confidence interval that $$\left(\overline X - z_{1-\alpha/2} \frac{\sigma}{\sqrt n} ,\overline  X + z_{1-\alpha/2} \frac{\sigma}{\sqrt n} \right)$$
#### Where $\sigma^2$ is unknown.
Let $X_1, \dots, X_n$ be a random sample of a population with distribution $N(\mu, \sigma^2)$, with both $\mu$ and $\sigma^2$ unknown.  Then we know that $$Q= \frac{\overline X-\mu}{S/\sqrt n} \sim t(n-1)$$
The $Q$ is a pivotal quantity for $\mu$. We have that $t$ distribution is symmetric and unimodal, so we only need a quantile $t^{1-\alpha/2}_{n-1}$, being $P(Q \le t^{1-\alpha/2}_{n-1}) = 1-\alpha/2$. Then by a similar argument as above we van get that  $$P(-t^{1-\alpha/2}_{n-1} \le Q \le t^{1-\alpha/2}_{n-1}) = 1-\alpha$$
then equivalently $$P\left(\overline X-t^{1-\alpha/2}_{n-1} \frac{S}{\sqrt n} < \mu<\overline X+t^{1-\alpha/2}_{n-1} \frac{S}{\sqrt n} \right)  = 1-\alpha$$
We get that the $(1-\alpha)$ confidence interval that $$\left(\overline X-t^{1-\alpha/2}_{n-1} \frac{S}{\sqrt n},\overline X+t^{1-\alpha/2}_{n-1} \frac{S}{\sqrt n} \right)$$
### Interval for the variance
Let $X_1, \dots, X_n$ be a random sample of a population with distribution $N(\mu, \sigma^2)$, with both $\mu$ and $\sigma^2$ unknown. We know that $$Q=\frac{(n-1) S^2}{\sigma²} \sim \chi^2(n-1)$$
$Q$ is a pivotal quantity, we need the quantiles $\chi^{\alpha/2}_{n-1}, \chi^{1-\alpha/2}_{n-1}\in \Bbb R$ such that $$P\left(\chi^{\alpha/2}_{n-1} < Q <\chi^{1-\alpha/2}_{n-1}\right) = 1-\alpha$$
which is equivalent to $$P \left(\frac{(n-1)S^2}{\chi^{1-\alpha/2}_{n-1}}< \sigma^2 < \frac{(n-1)S^2}{\chi^{\alpha/2}_{n-1}}\right)=1-\alpha $$
The interval of $(1-\alpha)$ confidence for $\sigma^2$ is $$\left(\frac{(n-1)S^2}{\chi^{1-\alpha/2}_{n-1}}, \frac{(n-1)S^2}{\chi^{\alpha/2}_{n-1}}\right)$$
### For difference in means for independent normal

Let $X_1, \dots, X_n$ is a random sample of $N(\mu_x, \sigma^2_x)$ and $Y_1, \dots, Y_m$ be a random sample of $N(\mu_y, \sigma^2)$ where $Y_j$ and $X_j$ are independent.
#### Where $\sigma^2_x$ and $\sigma^2_y$  are known

Let $\overline X \sim N(\mu_x, \sigma^2_x/n)$ and $\overline Y \sim N(\mu_y, \sigma^2_y/m)$, then $$\overline X - \overline Y  \sim N\left(\mu_x - \mu_y, \frac{\sigma^2_x}{n}+ \frac{\sigma^2_y}{m}\right) $$
and get that $$Q = \frac{\overline X - \overline Y -(\mu_x-\mu_y)}{\sqrt{\frac{\sigma_x^2}{n}+ \frac{\sigma^2_y}{m}}} \sim N(0,1)$$Where $Q$ is a pivotal quantity, then similarly as we did for the mean for $1$ distribution, then we get that $z_{1-\alpha/2}$ be the $1-\alpha/2$ quantile, then we can get the $(1-\alpha)$ confidence interval $$\left((\overline X- \overline Y) - z_{1-\alpha/2}\sqrt{\frac{\sigma^2_x}{n} + \frac{\sigma_y^2}{m}},(\overline X- \overline Y) + z_{1-\alpha/2}\sqrt{\frac{\sigma^2_x}{n} + \frac{\sigma_y^2}{m}} \right)$$
#### Where $\sigma^2_x$ and $\sigma^2_y$  are known, but $\sigma^2 = \sigma^2_x = \sigma^2_y$ 

Then we have that $\dfrac{(n-1)S^2_x}{\sigma^2} \sim \chi^2(n-1)$, and $\dfrac{(m-1)S^2_y}{\sigma^2} \sim \chi^2(m-1)$, then $$\frac{1}{\sigma^2}\left((n-1) S^2_x + (m-1)S^2_y\right) \sim \chi^2(n+m-2)$$
WE need to define $$S^2_p = \frac{(n-1)S^2_x +(m-1)S^2_y}{n+m-2}$$
if we do the maths, we get that $$Q=\frac{\overline X- \overline Y - (\mu_x-\mu_y)}{S_p \sqrt{\frac{1}{n}+ \frac{1}{m}}} \sim t(n+m-2) $$
$Q$ is the pivotal quantity for $\mu_x-\mu_y$. Then similarly as we did for when $\sigma^2$ was unknown, let $t^{1-\alpha/2}_{n+m-2}$ be the $1-\alpha/2$ quantile of the $t(n+m-2)$ distribution. Then the interval of $(1-\alpha)$ confidence is $$\left((\overline X - \overline Y)-t^{1-\alpha/2}_{n+m-2} S_p\sqrt{\frac{1}{n}+\frac{1}{m}},(\overline X - \overline Y)+t^{1-\alpha/2}_{n+m-2} S_p\sqrt{\frac{1}{n}+\frac{1}{m}} \right)$$
#### For $\sigma^2_x \ne \sigma^2_y$ and unknown 
This case is the known as the Behrens-Fisher problem, an unsolved problem in statistics. There are different approaches, but nothing concrete (maybe i am indeed kinda dumb)

### Quotient of variances of independent normals
Then we know that $$\frac{(n-1)S^2_x}{\sigma^2_x} \sim \chi^2(n-1)\qquad \frac{(m-1)S^2_y}{\sigma^2_x} \sim \chi^2(m-1)$$then $$Q=\frac{S_x^2/\sigma^2_x}{S^2_y/\sigma^2_y} \sim F(n-1, m-1)$$
$Q$ is the pivotal quantity for $\sigma^2_x/\sigma^2_y$, then we consider the quantiles $f^{\alpha/2}_{n-1, m-1}, f^{1-\alpha/2}_{n-1, m-1}$ such that $$P\left(f^{\alpha/2}_{n-1, m-1}< Q <f^{1-\alpha/2}_{n-1, m-1}\right) =1-\alpha$$
Then we have that equivalently that $$P\left(\frac{1}{f^{1-\alpha/2}_{n-1, m-1}} \frac{S_x^2}{S^2_y} < \frac{\sigma^2_x}{\sigma^2_y} < \frac{1}{f^{\alpha/2}_{n-1, m-1}} \frac{S_x^2}{S^2_y}\right) = 1 - \alpha$$
Then the interval of $(1-\alpha)$ confidence for $\sigma^2_x/\sigma^2_y$ is given by $$\left(\frac{1}{f^{1-\alpha/2}_{n-1, m-1}} \frac{S_x^2}{S^2_y} ,\frac{1}{f^{\alpha/2}_{n-1, m-1}} \frac{S_x^2}{S^2_y}\right)$$
We actually have by some symmetry of the F-distribution we have that $$f^{\alpha/2}_{n , m} = \frac{1}{f^{1-\alpha/2}_{m, n}}$$
With this we can rewrite the the confidence interval as $$\left(\frac{1}{f^{1-\alpha/2}_{n-1, m-1}} \frac{S_x^2}{S^2_y} ,{f^{1-\alpha/2}_{m-1, n-1}} \frac{S_x^2}{S^2_y}\right)$$