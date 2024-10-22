---
tags:
  - Analysis
  - LinearAlgebra
---
Subjects: [[Metric and Normed Spaces]], [[Linear Algebra]]
Links: [[Space of Linear Transformations]], [[Inner Products and Norms]], [[Normed Spaces]]
### Norm in $\mathcal{L}(\Bbb R^n, \Bbb R^m)$
************Prop:************ If $L \in \mathcal{L}(\Bbb R^n, \Bbb R^m)$, then there exists a $k > 0$, for any ${x} \in \Bbb R^n$ such that
$$ \|L(x)\| \le k \|x\| $$

**Prop:** If $L \in \mathcal{L}(\Bbb R^n, \Bbb R^m)$, then $L$ is uniformly continuous on $\Bbb R^n$.
**Lemma:** If the linear function $T :\Bbb R^n\to \Bbb R^n$ is an isomorphism (and so invertible) then there is $\mu >0$ such that for all $\mathbf x\in\Bbb R^n$

$$ \|Tx\| \le \mu\|x\| \quad \text{ and } \|T^{-1}x\| \ge \frac{1}{\mu}\|x\| $$

Let $\mathcal{L}(n,m) = \mathcal{L}(\Bbb R^n, \Bbb R^m)$ for the rest of this section.

**Def:** Let $L \in \mathcal{L}(n,m)$, and the set associated with $L$, $U_L$ as:

$$ U_L = \{k > 0 \mid \forall x \in \Bbb R^n[\|L(x) \| \le k \|x\|]\} $$
We will define the $\|\cdot\|_{\mathcal{L}(n,m)} : \mathcal L(n,m) \to \Bbb R^n$ as
$$ \|L\|_{\mathcal L} := \inf U_L = \sup_{{\hat u}\in \mathbb{S}^{n-1}}\|L({\hat u})\| $$
********Prop:******** If $L \in \mathcal L(n,m)$, then for any $\mathbf x \in \Bbb R^n$
$$ \|L(x) \| \le \|L\|_{\mathcal L(n,m)}\|x\| $$
**Th:** $\|\cdot\|_{\mathcal L(n,m)}$ is a norm on $\mathcal L(n,m)$

We can check that this is the only type of norm we need for linear transformations between finite dimensional normed spaces since, since every normed space of finite dimension that has as a base field $\Bbb R$ is isometric to some $\Bbb R^n$. So the norm of the operators also gets kinda "isometrized" by this process. 

This is actually a special case to what happens to [[Bounded Linear Operators]]