---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]

Let $f$ be defined on $[a,b]$. If $P=\{x_i\}_{i=0}^n$ is a partition of $[a,b]$, and ${\Delta f_k = f(x_k)-f(x_{k-1})}$, for all $k \le n$. If there’s an $M >0$ such that:

$$ \sum_{k=1}^n |\Delta f_k| \le M $$

For all partitions $P$, then we say that $f$ is of _bounded variation on_ $[a,b]$

If $f$ is monotonic on $[a,b]$, then $f$ is of bounded variation on $[a,b]$

$(*)$ If $f:E\subseteq\Bbb R \to \Bbb R$ is monotonic, then it is differentiable almost everywhere.

If $f$ is continuous on $[a,b]$, and $f'$ exists and is bounded on the interior then $f$ is of bounded variation on $[a,b]$.

If $f$ is of bounded variation on $[a,b]$, and it is bounded by $M$, then for any $x \in [a,b]$

$$ |f(x)| \le |f(a)| + M $$

We can say that the set of all the functions of bounded variation on $[a,b]$ as $BV[a,b]$

### Total Variation

Let $f: [a,b] \to \Bbb R$, the _total variation of $f$ on $[a,b]$_ is defined as:

$$ V_f(a,b)=\sup_{P\in \wp_I}\sum_P |\Delta f_i| $$

In general $V_f(a,b) \ge 0$, and if $V_f(a,b) = 0$ iff $f$ is a constant on $[a,b]$

Both $V(f)$ and $V_f(a,b)$ will be used, the first if the domain is clear by the context and it is unchanging, the latter when the domain is changing or to clarify.

If $V_I(f) < \infty$, iff ${\alpha \in BV(I)}$ .

In particular, if $f$ is continuous on $[a,b]$, and differentiable on $(a,b)$, with $|f'(x)| \le M$, for some $M >0$, then:

$$ V_f \le M(b-a) $$

If $f$ is differentiable and it’s derivative is Riemann Integrable then:

$$ V_f =\int_I |f '| $$

If $f, g \in BV(I),$ and $c, d\in \Bbb R$, then $cf+dg, fg \in BV(I)$, and

$$ V_{cf+dg} \le |c|V_f + |d|V_g \text{ ,and } V_{fg} \le AV_f + BV_g $$

where $A = \sup_{x\in I}|g(x)|$ and $B = \sup_{x\in I}|f(x)|$

Let $f\in BV(I)$ and bounded away from zero, is bounded away from zero iff ${\exists m> 0\forall x\in I(m \le }|f(x)|)$, then $1/f \in BV(I)$, and $V_{1/f} \le \frac{V_f}{m^2}$

### Additive Property of Total Variation

If $f \in BV([a,b])$, and $c \in (a,b)$, then $f\in BV([a,c]), BV([c,b])$ , and:

$$ V_f{(a,c)} +V_f{(c,b)} = V_f{(a,b)} $$

If $\alpha \in BV([a,b])$, and $[c,d] \subseteq [a,b]$, then $\alpha \in BV([c,d])$, and:

$$ V_{[c,d]}(\alpha) \le V_{[a,b]}(\alpha) $$

If $f \in BV([a,b])$, then $V: [a,b] \to \Bbb R$, then $V(x) = V_f{(a,x)}$, and $V - f$ are both monotonically increasing.

Let $f$ be a function of bounded variation iff it can be expressed as a difference of two increasing functions

$(*)$ Then if $f$ is of bounded variation, then it is differentiable almost everywhere

### Continuous functions of Bounded Variation

Let $f$ be a of bounded variation on $[a,b]$, and $V(x) = V_f(a,x)$. $f$ is continuous at $x_0$ iff $V$ is continuous at $x_0$