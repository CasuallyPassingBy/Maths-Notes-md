---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measurable Functions]], [[Measure Spaces and Measurable Spaces]], [[Measures]]

**Th:** if $\{f_n \mid n < \omega\}$ is a sequence of extended real values measurable functions on a measurable space $X$, then the following functions are measurable:
- $h(x) = \sup\{f_n(x) \mid n < \omega\}$
- $g(x) = \inf\{f_n(x) \mid n < \omega\}$
- $f^*(x) = \limsup_{n \to \infty} f_n(x)$
- $f_*(x) = \liminf_{n \to \infty} f_n(x)$

**Cor:** if $\{f_n \mid n < \omega\}$ is a sequence of extended real values measurable functions on a measurable space $X$, then the set of convergence of the sequence $\{f_n\mid n <\omega\}$, i.e., the set $$\left\{x\in X \; \left\rvert \; \limsup_{n\to \infty} f_n(x) = \liminf_{n\to \infty} f_n(x)\right.\right\},$$has a measurable intersection with every measurable set, and consequently, that the function $f$, defined by $f(x) = \lim_{n \to \infty} f_n(x)$ at every $x$ for which the limits exists, is measurable function. 

**Def:** A function $f$, defined on a measurable space $X$, is called *simple* if there is a finite, disjoint class $\{E_1, \dots, E_n\}$ me measurable sets and a finte set $\{\alpha_1, \dots, \alpha_n\}$ of real numbers such that $$f(x) = \sum_{i = 1}^n \alpha_i\chi_{E_i}(x).$$
**Th:** Every extended real valued measurable function $f$ is the limit of a sequence $\{f_n \mid n < \omega\}$ of simple functions; if $f$ is non negative, then each $f_n$ may be taken non negative and the sequence $\{f_n \mid n <\omega\}$ may be assumed increasing. 

If $f$ is bounded, then the sequence $\{f_n\mid n <\omega\}$ can be made to converge uniformly.

**Def:** An *elementary function* is defined the same way as a simple function, the only change being that the number of sets $\{E_n \mid n <\omega\}$ is allowed to be countably infinite.

**Prop:** Every real valued measurable function $f$ is the limit of uniformly convergent sequence of elementary functions. 

**Prop:** If we disregard the results that requiere order of $\Bbb R$, then the results above can be extended to for complex valued sequences of measurable functions. 

# Convergence

**Def:** If a certain proposition concerning points of a measure space is true for every point, with exception at most of a set of measure zero, it is customary to say that the proposition is true *almost everywhere* or *a.e.*
**Def:** A function $f$ is called *essentially bounded* if it is bounded a.e., i.e., if there exists a $M >0$ such that $\mu(\{x\in X \mid |f(x)| > c\}) = 0$. The infimum of the of the valued of $M$ for which the statement is true is called the *essential supremum* of $|f|$, abbreviated to $\text{ess sup}(|f|)$.

**Def:** Let $\{f_n \mid n <\omega\}$ be a sequence of extended real valued functions which converges a.e. on the measure space $X$ to the limit function $f$. This means, of course, that there exists a set $E_0$ of measure zero such that, if $x\notin E_0$ and $\varepsilon>0$, then there exists $N \in \omega$, such that
- if $f(x) = -\infty$, then $f_n(x) < -1/\varepsilon$
- If $f(x) \in \Bbb R$, then $|f_n(x)- f(x)| < \varepsilon$
- if $f(x) = \infty$ then $f_n(x) < 1/\varepsilon$
whenever $n \ge N$. 

**Def:** We shall say that a sequence $\{f_n \mid n <\omega\}$ of real valued function is *fundamental a.e.* if there exists a set $E_0$ of measure zero such that, if $x\notin E_0$ and $\varepsilon>0$, then there's an integer $N <\omega$, with the property if $n, m \ge N$ $$|f_n(x) - f_m(x)|<\varepsilon.$$
**Obs:** It is clear that if a sequence converges to a finite valued limit function a.e., then it is fundamental a.e., and conversely, that corresponding to a sequence which is fundamental a.e. there always exists a finite valued limit function to which it converges a.e.

**Obs:** On the space of measurable functions being equal a.e. is an equivalence relation. Let $f, g, h: X\to \Bbb R$ measurable functions, then:
- $f = f$ a.e.
- If $f = g$ a.e., then $g = f$ a.e.
- If $f = g$ and $g = h$ a.e., then $f = h$ a.e.

**Prop:** If $f$ is any real valued, Lebesgue measurable function on the real line, then there exista a Borel measurable function $g$ such that $f = g$ a.e.
 
**Def:** The sequence $\{f_n \mid n < \omega\}$ converges to $f$ *uniformly a.e.* if there's a set $E_0$ of measure zero that, for every $\varepsilon>0$, there's an integer $N <\omega$ can be found with the property that for every $x \in X\setminus E_0$, $$|f_n(x) - f(x) |< \varepsilon.$$
**Egoroff's Theorem:** If $E$ is a measurable set of finite measure and if $\{f_n\mid n <\omega\}$ is a sequence of a.e. finite valued measurable functions which converges a.e. on $E$ to a finite valued measurable function $f$, then, for every $\varepsilon>0$, there's exists a measurable subset $F\subseteq E$ such that $\mu(F) < \varepsilon$ and such that the sequence $\{f_n \mid n <\omega\}$ converges to $f$ uniformly on $E\setminus F$.

**Def:** A sequence $\{f_n \mid n <\omega\}$ of a.e. finite valued measurable functions will be said to the measurable function $f$ *almost uniformly*, if for every $\varepsilon>0$, there's a measurable set $F$ such that $\mu(F) < \varepsilon$ and such that the sequence $\{f_n\}$ converges uniformly to $f$ uniformly on $X\setminus F$. 

**Obs:** We see that Egoroff's theorem assets that on a set of finite measure convergence a.e. implies almost uniform convergence. 

**Cor:** If $E$ is a measurable set of positive finite measure, and if $\{f_n\mid n <\omega\}$ is a sequence of a.e. finite valued measurable functions which is fundamental a.e., then there exist $M>0$ and an $F\subseteq E$ of positive measure such that for every $n < \omega$, and every $x\in F$ $|f(x)| \le c$. 

**Cor:** If $E$ is a measurable set of a $\sigma$-finite measure, if $\{f_n\mid n <\omega\}$ is a sequence of a.e. finite valued measurable functions which converges a.e. on $E$ to a finite valued measurable function, then there exists a sequence of $\{E_m \mid m < \omega\}$ of measurable sets such that $\mu\left(E\setminus\bigcup_{m <\omega} E_n\right) = 0$ and such that the sequence $\{f_n\}$ converges uniformly on each $E_m$. 

**Prop:** If $\{f_n\mid n <\omega\}$ is a sequence of measurable functions which converges to $f$ almost uniformly, then $\{f_n \mid n <\omega\}$ to $f$ a.e.

# Convergence in Measure

**Th:** Suppose that $f$ and $f_n$, $n <\omega$ are real valued measurable functions on a set $E$ of finite measure, and write for every $\varepsilon >0$, $$E_n(\varepsilon) := \{x \in X \mid |f_n(x) - f(x)| \ge \varepsilon\}, \qquad n < \omega.$$The sequence $\{f_n\mid n <\omega\}$ converges to $f$ a.e. on $E$ iff $$\lim_{n \to \infty} \mu\left(E\cap \bigcup_{m = n}^\infty E_m(\varepsilon)\right) = 0$$for every $\varepsilon>0$.

**Def:** A sequence $\{f_n \mid n  <\omega\}$ of a.e. finite valued, measurable functions *converges in measure* to the measurable function $f$ if, for every $\varepsilon>0$, $\lim_{n\to\infty}\mu(\{x\in X\mid |f_n(x) - f(x)| \ge \varepsilon\})=0$. In accordance with our general comment on different kinds of convergence, we shall say that a sequence $\{f_n \mid n <\omega\}$ of a.e. finite valued measurable functions is *fundamental in measure* if, for every $\varepsilon >0$, $$\lim_{n, m \to \infty} \mu(\{x\in X\mid |f_n(x) - f_m(x)| \ge \varepsilon\}) = 0.$$
**Obs:** Every subsequence of a sequence which is fundamental in measure is fundamental in measure. 

**Obs:** If a sequence of finite valued measurable functions converges a.e. to a finite limit (or is fundamental a.e.) on a set $E$ of finite measure, then it converges in measure (or is fundamental in measure) on $E$. 

**Obs:** If $X = \Bbb N$ is the set of all integers, $\mathcal S= P(\Bbb N)$, and for every $E \in \cal S$, $\mu(E) := |E|$, then, for the measure space $(\Bbb N, P(\Bbb N), \mu)$, convergence in measure is equivalent to uniform convergence everywhere.  

**Obs:** On a set of infinite measure convergence a.e. implies convergence in measure. 

**Th:** Almost uniform convergence implies convergence in measure.

**Prop:** Every subsequence of a sequence which is fundamental in measure is fundamental in measure.

**Prop:** If $\{f_n\mid n <\omega\}$ converges in measure to $f$, then $\{f_n \mid n <\omega\}$ is fundamental in measure. If $\{f_n \mid n < \omega\}$ converges in measure to $g$ then $f = g$ a.e. 

**Obs:** There are the measure space $(X, \mathcal S, \mu)$ that are totally finite, and sequences of functions $\{f_n \mid n <\omega\}$ that converge in measure but there are no points that converges.

**Def:** a sequence of measurable functions is *uniformly fundamental in measure* if for every $\varepsilon> 0$ and $\delta>0$, there's a $N< \omega$ such that for all $m, n\ge N$, $$\mu(\{x \in X \mid |f_n(x) - f_m(x)|\ge \varepsilon\})<\delta. $$
**Th:** If $\{f_n\mid n <\omega\}$ is a sequence of measurable functions which is fundamental in measure, then some subsequence $\{f_{n_k}\mid k < \omega\}$ is almost uniformly fundamental.

**Th:** If $\{f_n\mid n <\omega\}$ is a sequence of measurable functions which is fundamental in measure, then there exists a measurable function $f$ such that $\{f_n \mid n <\omega\}$ converges in measure to $f$. 

**Prop:** Suppose the measure space $(X, \mathcal S, \mu)$ is totally finite, and let $\{f_n \mid n < \omega\}$ and $\{g_n \mid n <\omega\}$ be sequence of finite valued measurable functions converging in measure to $f$ and $g$ respectively. Then the following are true:
- If $\alpha, \beta\in \Bbb R$, then $\{\alpha f_n + \beta g_n \mid n < \omega\}$ converges in measure to $\alpha f+ \beta g$.
- $\{|f_n| \mid n <\omega\}$ converges to $|f|$. 
- If $f= 0$ a.e, then $\{f_n^2 \mid n <\omega\}$ converges in measure to $f^2$. 
- The sequence $\{f_n g \mid n <\omega\}$ converges in measure to $fg$.
- The sequence $\{f_n^2 \mid n <\omega\}$ converges in measure to $f^2$. 
- The sequence $\{f_n g_n \mid n <\omega\}$ converges in measure to $fg$.