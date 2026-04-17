---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]], [[Measure Theory]]
Links: [[Continuity on R]], [[Measures]], [[Signed and Complex Measures]]

**Def:** Suppose that $F$ is a real-valued function whose domain includes the interval $[a,b]$. Let $\scr S$ be the collection of finite squences $\{t_i\}_{ i <n+1}$ such that $$a\le t_0 < t_1<\dots < t_n \le b.$$Then $V_F[a,b]$, the *variation of $F$ over $[a,b]$*, is defined by $$V_F[a,b] := \sup\left\{\left.\sum_{i} |F(t_i)- F(t_i)| \;\right\rvert; \{t_i\}\in {\scr S}\right\}.$$The function $F$ is of *finite variation* or *bounded variation* on $[a,b]$ if $V_F[a,b]$ is finte. 
The *variation of $F$ over* the interval $(-\infty, b]$ and the *variation of $F$ over $\Bbb R$*, written $V_F(-\infty, b]$ and $V_F(-\infty, \infty)$, respectively, are defined in a similar way, now using sequences that belong to their respective domains. Similarly, we say that $F$ is finite variation over those intervals if the variation of $F$ is finite. If $F:\Bbb R\to\Bbb R$ is of finite variation, then the *variation* of $F$ is the function $V_F: \Bbb R\to\Bbb R$ defined by $V_F(x) := V_F(-\infty, x]$.

**Obs:** If $f$ is monotonic on $[a,b]$, then $f$ is of bounded variation on $[a,b]$

$(*)$ If $f:E\subseteq\Bbb R \to \Bbb R$ is monotonic, then it is differentiable almost everywhere.

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

Suppose that $\mu$ is a finite signed measure on $(\Bbb R, {\cal B}(\Bbb R))$. We can define a function $F_\mu: \Bbb R\to\Bbb R$ by letting  $$F_\mu(x) := \mu((-\infty, x]).$$We see that $V_{F_\mu}(-\infty, \infty) \le |\mu|(\Bbb R)$, and hence $F_\mu$ is of finte variation. 



If $f \in BV([a,b])$, and $c \in (a,b)$, then $f\in BV([a,c]), BV([c,b])$ , and:
$$ V_f{(a,c)} +V_f{(c,b)} = V_f{(a,b)} $$

If $\alpha \in BV([a,b])$, and $[c,d] \subseteq [a,b]$, then $\alpha \in BV([c,d])$, and:

$$ V_{[c,d]}(\alpha) \le V_{[a,b]}(\alpha) $$

If $f \in BV([a,b])$, then $V: [a,b] \to \Bbb R$, then $V(x) = V_f{(a,x)}$, and $V - f$ are both monotonically increasing.

Let $f$ be a function of bounded variation iff it can be expressed as a difference of two increasing functions

$(*)$ Then if $f$ is of bounded variation, then it is differentiable almost everywhere

Let $f$ be a of bounded variation on $[a,b]$, and $V(x) = V_f(a,x)$. $f$ is continuous at $x_0$ iff $V$ is continuous at $x_0$

