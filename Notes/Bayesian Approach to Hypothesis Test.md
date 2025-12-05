---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Bayesian Approach to Point Estimators]], [[Bayesian Approach to Interval Estimation]], [[Statistical Hypothesis Test]]

In the Bayesian approach, contrasting hypotheses means comparing the posterior probabilities of the parameter being in each region and choosing the hypothesis with higher probability

In the Bayesian context we also can make hypothesis contrast, and even more we can make hypothesis testing with more than $2$ hypothesis. $$H_1 : \theta\in \Theta_1,  \quad H_2 : \theta\in \Theta_2,\quad \cdots, H_J: \theta\in \Theta_J,$$where $\Theta_1,\dots, \Theta_J$ is a partition of the parametric space $\Theta$. 

Suppose that $X$ comes from a model $f(x\mid \theta)$ and would like to evaluate the hypothesis $$H_0: \theta \in \Theta_0\quad \text{vs} \quad H_1: \theta\in \Theta_1,$$where $\Theta_0$ and $\Theta_1$ are a partition of $\Theta$. We need to specify an initial distribution for the parameter $\theta$. If we were to have an initial density function $\pi(\theta)$, then it is possible to evaluate the two hypothesis a priori using the quotient $$ \frac{\tau_0}{\tau_1} = \frac{P(\theta\in \Theta_0)}{P(\theta\in \Theta_1)} = \frac{\int_{\theta\in \Theta_0 }\pi (\theta)\, d\theta}{\int_{\theta\in \Theta_1 }\pi (\theta)\, d\theta}.$$
Once observed the data, $X = x$, then we update the initial distribution through the a posteriori distribution $$\pi(\theta \mid x) \propto L(\theta\mid x )\pi (\theta),$$where $L(\theta\mid x)$ is the likelihood function. The two hypothesis can be contrasted now with respect to the a posteriori distribution $$\frac{p_0}{p_1} = \frac{P(\theta\in \Theta_0 \mid x)}{P(\theta\in \Theta_1 \mid x)} =\frac{\int_{\theta\in \Theta_0}\pi(\theta\mid x)\, d\theta}{\int_{\theta\in \Theta_1}\pi(\theta\mid x)\, d\theta}.$$
The Bayesian approach the contrast between the hypothesis is comparing the different distributions of the parameters and choose the one who has  a higher probability. We would choose the hypothesis with larger prior probability if no data were available

Usually we propose the statistic known as the *Bayes factor* defined as $$\text{BF}  =\frac{p_0/p_1}{\tau_0/\tau_1},$$as a measures of the evidence being of favor the null hypothesis. 

The Bayes factor measure how much the data updates our belief in favor of $H_0$ relative to $H_1$. If $\text{BF} >1$, the data provides evidence for $H_0$. Note that the Bayes factor can also be written as $$\text{BF} = \frac{\pi(x \mid H_0)}{\pi(x \mid H_1)} $$since the posterior odds $=$ Bayes factor $\times$ prior odds. 

Alternatively, we can treat each hypothesis as a separate model and assign prior probabilities directly to the models themselves. The evaluation of the probability relative to the hypothesis or the models can be done using the a posteriori of the associated model $$\pi(H_j\mid x ) \propto \pi(x \mid H_j) \pi(H_j),$$where $\tau_j = \pi(H_j)$, and $p_j = \pi(H_j \mid x )$. Additionally, we see know that $$\pi(x\mid H_j) = \int \pi(x\mid \theta) \pi(\theta\mid H_j)\, d\theta $$is the marginal likelihood of the $H_j$ model, and $\pi(\theta\mid H_j)$ is the initial distribution for $\theta$ given $H_j$ true.

The marginal likelihood is the probability of the observed data after averaging over all possible parameter values allowed by the model.

his means that if we want to compare two hypothesis $H_0$ and $H_1$, we need to calculate $\pi(H_0\mid x)$ and $\pi(H_1\mid x)$, and these probabilities can be compared using the Bayes factor. 