---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]], [[Measure Theory]]
Links: [[Continuity on R]], [[Measures]], [[Signed and Complex Measures]]

**Def:** Suppose that $F$ is a real-valued function whose domain includes the interval $[a,b]$. Let $\scr S$ be the collection of finite squences $\{t_i\}_{ i <n+1}$ such that $$a\le t_0 < t_1<\dots < t_n \le b.$$Then $V_F[a,b]$, the *variation of $F$ over $[a,b]$*, is defined by $$V_F[a,b] := \sup\left\{\left.\sum_{i} |F(t_i)- F(t_i)| \;\right\rvert; \{t_i\}\in {\scr S}\right\}.$$The function $F$ is of *finite variation* or *bounded variation* on $[a,b]$ if $V_F[a,b]$ is finte. 
The *variation of $F$ over* the interval $(-\infty, b]$ and the *variation of $F$ over $\Bbb R$*, written $V_F(-\infty, b]$ and $V_F(-\infty, \infty)$, respectively, are defined in a similar way, now using sequences that belong to their respective domains. Similarly, we say that $F$ is finite variation over those intervals if the variation of $F$ is finite. If $F:\Bbb R\to\Bbb R$ is of finite variation, then the *variation* of $F$ is the function $V_F: \Bbb R\to\Bbb R$ defined by $V_F(x) := V_F(-\infty, x]$.

**Obs:** If $f$ is monotonic on $[a,b]$, then $f$ is of bounded variation on $[a,b]$

If $f$ is continuous on $[a,b]$, and $f'$ exists and is bounded on the interior then $f$ is of bounded variation on $[a,b]$.

If $f$ is of bounded variation on $[a,b]$, and it is bounded by $M$, then for any $x \in [a,b]$
$$ |f(x)| \le |f(a)| + M $$

We can say that the set of all the functions of bounded variation on $[a,b]$ as $BV[a,b]$

In particular, if $f$ is continuous on $[a,b]$, and differentiable on $(a,b)$, with $|f'(x)| \le M$, for some $M >0$, then:
$$ V_f \le M(b-a) $$

If $f$ is differentiable and it’s derivative is Riemann Integrable then:$$ V_f =\int_I |f '| $$
If $f, g \in BV(I),$ and $c, d\in \Bbb R$, then $cf+dg, fg \in BV(I)$, and
$$ V_{cf+dg} \le |c|V_f + |d|V_g \text{ ,and } V_{fg} \le AV_f + BV_g $$

where $A = \sup_{x\in I}|g(x)|$ and $B = \sup_{x\in I}|f(x)|$. We get that $BV(I)$ is an algebra. 

Let $f\in BV(I)$ and bounded away from zero, is bounded away from zero iff ${\exists m> 0\forall x\in I(m \le }|f(x)|)$, then $1/f \in BV(I)$, and $V_{1/f} \le \frac{V_f}{m^2}$

Suppose that $\mu$ is a finite signed measure on $(\Bbb R, {\cal B}(\Bbb R))$. We can define a function $F_\mu: \Bbb R\to\Bbb R$ by letting  $$F_\mu(x) := \mu((-\infty, x]).$$We see that $V_{F_\mu}(-\infty, \infty) \le |\mu|(\Bbb R)$, and hence $F_\mu$ is of finte variation. It is easy to check the function $F_\mu$ is continuous iff $\mu(\{x\}) = 0$ holds for each $x\in \Bbb R$. 

Suppose that $F:\Bbb R \to\Bbb R$ is of finite variation. It is easy to check that $F$ is bounded and if $-\infty<a<b<\infty$, then  $$V_F(-\infty, b] = V_F(-\infty, a] + V_F[a,b]. $$Furthermore, if $b\in \Bbb R$, then $$V_F(-\infty, b] = \lim_{a\to-\infty}V_F[a, b]. $$ Similarly, if $[a,c]$ and if $F$ is right-continuous at $a$, then $$V_F[a, c] = \lim_{b\to a^+}V_F[b,c]. $$

**Lemma:** Let $F$ be a function of finite variation on $\Bbb R$. Then
- $V_F$ is bounded and non-decreasing,
- $V_F$ vanishes at $-\infty$, and
- if $F$ is right-continuous, then $V_F$ is right continuous.

**Prop:** If $F:\Bbb R\to\Bbb R$ is continuous and of finite variation, then $V_F:\Bbb R \to\Bbb R$ is continuous.

**Prop:** Let $F$ be a function of finite variation on $\Bbb R$. Then there are bounded non-decreasing functions $F_1$ and $F_2$ such that $F = F_1-F_2$. 

**Prop:** If $F$ is of finite variation on $\Bbb R$, then the limits $\lim\limits_{x\to-\infty}F(x)$ and $\lim\limits_{x\to\infty}F(x)$ exist. 

**Prop:** We see that we can define a bijection $\mu \mapsto F_\mu$ between the set of all signed measures on $(\Bbb R, {\cal B}(\Bbb R))$ and the set of all right-continuous functions of finite variation that vanish at $-\infty$.

**Def:** A function $F:\Bbb R\to\Bbb R$ is *absolutely continuous* if for each $\varepsilon >0$ there is a $\delta> 0$ such that $\sum_i |F(t_i)- F(s_i)| <\varepsilon$ holds whenever $\{(s_i, t_i)\}$ is finite sequence of disjoint open intervals for which $\sum_i(t_i-s_i)<\delta$. 

**Obs:** We see that every absolutely continuous function is continuous and, in fact, uniformly continuous. There are, however, functions that are uniformly continuous and of finite variation, but are not absolutely continuous. 

**Prop:** If $F:\Bbb R\to\Bbb R$ is absolutely continuous, then $F$ is finite variation on each closed bounded interval.

**Lemma:** If $F:\Bbb R\to \Bbb R$ is absolutely continuous and of finite variation, then $V_F$ is absolutely continuous. 

**Prop:** Let $\mu$ be a finite signed measure on $(\Bbb R, {\cal B}(\Bbb R))$, and let $F_\mu: \Bbb R\to\Bbb R$ defined by $$F_\mu(x) := \mu((-\infty, x]). $$Then $F_\mu$ is absolutely continuous iff $\mu$ is absolutely continuous with respect to Lebesgue measure.

**Prop:** The function $F: \Bbb R\to \Bbb R$ that can be written in the form $$F(x) := \int_
{-\infty}^xf(t)\, dt$$for some $f\in {\scr L}^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$ are exactly the absolutely continuous functions of finite variation that vanish at $-\infty$.

**Prop:** If $F: \Bbb R\to \Bbb R$ is absolutely continuous, then $F$ is of finite variation on each bounded interval.

**Prop:** Let $\mu$ be a finite signed measure on $(\Bbb R, {\cal B}(\Bbb R))$. Then  $$V_{F_\mu}(-\infty, x] = |\mu|((-\infty, x]).$$