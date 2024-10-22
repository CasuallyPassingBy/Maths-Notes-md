---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]]

We define the following partial derivatives as follows

$$ \begin{align*} \frac{\partial}{\partial z} &= \frac{1}{2}\left(\frac{\partial}{\partial x} +\frac{1}{i}\frac{\partial}{\partial y}\right)=\frac{1}{2}\left(\frac{\partial}{\partial x} -{i}\frac{\partial}{\partial y}\right) \\ \frac{\partial}{\partial \overline z} &= \frac{1}{2}\left(\frac{\partial}{\partial x} -\frac{1}{i}\frac{\partial}{\partial y}\right)=\frac{1}{2}\left(\frac{\partial}{\partial x} +{i}\frac{\partial}{\partial y}\right) \end{align*} $$

this operators are called the **********************Wirtinger derivatives.********************** These derivatives can be extended to $\Bbb C^n$, where they play important roles to understand better the functions from $\Bbb C^n$.

************Prop:************ A function $f:A\to \Bbb C$ is holomorphic iff

$$ \frac{\partial f}{\partial \overline z} =0 $$

meaning $f$ is only dependent on $z$

************Prop:************ If $f$ is holomorphic, then $f' = \frac{\partial f}{\partial z}$

**********Prop:********** the Wirtenger Derivatives have the following properties

**********Linearity:********** Let $f,g :A \to \Bbb C$, and be $\cal C^1$, and $\alpha, \beta \in \Bbb C$ then

$$ \begin{align*}\frac{\partial}{\partial z} \left(\alpha f+\beta g\right) &= \alpha\frac{\partial f}{\partial z} + \beta\frac{\partial g}{\partial z} \\ \frac{\partial}{\partial\bar{z}} \left(\alpha f+\beta g\right) &= \alpha\frac{\partial f}{\partial\bar{z}} + \beta\frac{\partial g}{\partial\bar{z}}\end{align*} $$

**Product rule**Let $f,g :A \to \Bbb C$, and be $\cal C^1$, then

$$ \begin{align*} \frac{\partial}{\partial z} (f\cdot g) &= \frac{\partial f}{\partial z}\cdot g + f\cdot\frac{\partial g}{\partial z} \\ \frac{\partial}{\partial\bar{z}} (f\cdot g) &= \frac{\partial f}{\partial\bar{z}}\cdot g + f\cdot\frac{\partial g}{\partial\bar{z}} \end{align*} $$

************************Chain rule:************************ If $f: A\to \Bbb C$ and $g:B\to \Bbb C$, both $\cal C^1$, and $f[A] \subseteq B$ then

$$ \begin{align*} \frac{\partial}{\partial z} (f\circ g) &= \left(\frac{\partial f}{\partial z}\circ g \right) \frac{\partial g}{\partial z} + \left(\frac{\partial f}{\partial\bar{z}}\circ g \right) \frac{\partial\bar{g}}{\partial z} \\\frac{\partial}{\partial\bar{z}} (f\circ g) &= \left(\frac{\partial f}{\partial z}\circ g \right)\frac{\partial g}{\partial\bar{z}}+ \left(\frac{\partial f}{\partial\bar{z}}\circ g \right) \frac{\partial\bar{g}}{\partial\bar{z}}\end{align*} $$

************************Conjugation:************************ If $f:A \to \Bbb C$, and $f$ is $\cal C^1$ then

$$ \begin{align*}\overline{\left(\frac{\partial f}{\partial z}\right)} &= \frac{\partial \bar{f}}{\partial \bar{z}} \\ \overline{\left(\frac{\partial f}{\partial \bar{z}}\right)} &= \frac{\partial \bar{f}}{\partial z}\end{align*} $$

************Prop:************ Let $A$ be an open set of $\Bbb C$, and $A^* =\{z \mid \overline z\in A\}$. Suppose $f$ is holomorphic on $A$, and define $g$ on $A^*$ by $g(z) = \overline{f(\overline z)}$. Then $g$ is holomorphic on $A^*$ and $g'(z) = \overline{f'(\overline z)}$
