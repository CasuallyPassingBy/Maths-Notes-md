---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Point Estimation]]

The usual approach, called frequentest, we have no information about the parameter, but in the Bayesian approach, we actually pre suppose some information about the parameter, and we *update* our information. This updating of information is called *Bayesian Inference*, makes such that the estimator behaves like a random variable. 

First we need:
- The likelihood $L(\theta \mid \underline x)$ that represents the information that there's on the data
- $\pi(\theta)$ is a probability distribution, that is known as the *initial or a priori distribution* , and describes certain subjective ideas of that we have about the value of $\theta$. This ideas are external to the data and can be deduced from past experience of expert knowledge

The inference is expressed through the *final, a posterior , or posterior distribution* of the parameters, denoted as $\pi (\theta \mid x)$, and is is obtained through Bayes' Theorem as $$\pi(\theta\mid \underline x) = \dfrac{L(\theta \mid \underline x) \pi (\theta)}{\int_{\Theta} L(\theta \mid \underline x) \pi (\theta) \, d\theta}$$
In a lot of cases the selection of the initial distribution also contemplates the possibility of calculating the closed form of the denominator of the final distribution. A particular case of this selection is given by the *Conjugate Families*

**Def:** An initial distribution $\pi(\theta)$ is conjugate if for $\pi(\theta)\in \mathcal P$, and $L(\theta\mid \underline x) \in \mathcal F$, we have that $\pi(\theta\mid \underline x) \in \mathcal P$, where $\mathcal P$ and $\mathcal F$ are family of distributions

In practice we actually just look at $$L(\theta \mid \underline x) \pi (\theta)$$ and look if it is proportional to some known distribution. 