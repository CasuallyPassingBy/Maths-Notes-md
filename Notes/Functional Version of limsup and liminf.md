---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Functional Limits in R]], [[limsup and liminf]]

Let $f: E \to\Bbb R$ and $a$ a limit point of $E$. Then we can define

$$ \limsup_{x \to a} f(x) := \lim_{\varepsilon \to 0}(\sup\{ f(x)\mid x \in E \cap B_\varepsilon(a)\setminus a\}) $$

and

$$ \liminf_{x\to a}f(x) := \lim_{\varepsilon \to 0}(\inf\{f(x) \mid x \in E \cap B_{\varepsilon}(a) \setminus a\}) $$

We see that $\varepsilon$ shrinks, the supremum of the function over the ball is monotone decreasing, so we have that

$$ \limsup_{x \to a} f(x) := \inf_{\varepsilon >0}(\sup\{ f(x)\mid x \in E \cap B_\varepsilon(a)\setminus a\}) $$

and, similarly

$$ \liminf_{x\to a}f(x) := \sup_{\varepsilon > 0}(\inf\{f(x) \mid x \in E \cap B_{\varepsilon}(a) \setminus a\}) $$
I think that we can think we can use similar to a definition using arbitrary sequences such that $x_n \to x_0$ and $x_n \ne x_0$ for all $n\in \Bbb N$, then it has the property that

$$ \limsup_{k \to \infty} f(x_k) = \limsup_{x\to x_0} f(x) \qquad \liminf_{k \to \infty} f(x_k) = \liminf_{x\to x_0} f(x) $$