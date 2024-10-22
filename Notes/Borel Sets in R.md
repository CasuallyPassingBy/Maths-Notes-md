---
tags:
  - RealAnalysis
  - MeasureTheory
---
Subjects: [[Real Analysis]], [[Measure Theory]]
Links: [[Open and Closed Sets in R]], [[Real Numbers]], [[Sigma Algebra]]

We define the *Borel sets* as those sets of reals that can be obtained from open and closed sets by means of repeatedly taking countable unions and intersections. 

**Def:** A set $B \subseteq \Bbb R$ is *Borel* if it belongs to every system of sets $\mathcal S\subseteq \mathcal P(\Bbb R)$ with the following properties:
- All open sets and closed sets belong to $\mathcal S$
- If $B_n \in S$ for each $n \in \Bbb N$, then $\bigcup_{n  \in \Bbb N} B_n$ and  $\bigcap_{n  \in \Bbb N} B_n$ belong to $\mathcal S$
$\mathcal B$ denotes the system of all Borel sets

In other words, $\mathcal B = \bigcap \{\mathcal S \subseteq \mathcal P(\Bbb R)\mid \mathcal S \text{ with both properties}\}$ is the smallest collection of sets of reals that contains all open and all closed sets and is "closed" under countable unions and intersections. 

**Th:** The collection $\mathcal B$ of all Borel sets is a $\sigma$-algebra of subsets of $\Bbb R$. 

# Borel Hierarchy

We can also generate the Borel sets, as the minimal $\sigma$-algebra that contains the open sets. 

We see that all open and all closed sets are Borel sets. We define $$\begin{align*}
{\mathbf \Sigma}_1^0&:= \{B \subseteq \Bbb R \mid B \text{ is open}\} \\
{\mathbf \Pi}_1^0&:= \{B \subseteq \Bbb R \mid B \text{ is closed}\} \\

\end{align*} 
$$
Thus ${\mathbf \Sigma}_1^0, {\mathbf \Pi}_1^0 \subseteq \mathcal B$. Next, countable unions and intersections of open sets must be Borel. Countable unions of open sets are open, and do not produce new sets; so we define $${\mathbf \Pi}_2^0 = \left\{B \subseteq \Bbb R\;\left|\; B = \bigcap_{n \in \Bbb N} B_n,\text{ where each } B_n \in \mathbf \Sigma^0_1  \right.\right\}$$
Clearly $\mathbf \Sigma_0^1 \subseteq \mathbf \Pi_2^0$, we actually see that $\mathbf \Pi_2^0$ is the set of all $G_\delta$ sets, and the inclusion is proper. Similarly, we define  $${\mathbf \Sigma}_2^0 = \left\{B \subseteq \Bbb R\;\left|\; B = \bigcap_{n \in \Bbb N} B_n,\text{ where each } B_n \in \mathbf \Pi^0_1  \right.\right\}$$
Clearly, we have that $\mathbf \Pi_1^0\subseteq \mathbf \Sigma_2^1$, and see that $\mathbf \Sigma_2^0$ is the set of all $F_\sigma$ sets, and the inclusion is proper. It is also true that $\mathbf \Pi_1^0 \subseteq \mathbf \Pi_2^0$, and $\mathbf \Sigma_1^0 \subseteq \mathbf \Sigma_2^0$. Similarly we can define $\mathbf \Delta_1^0 = \mathbf \Pi_1^0 \cap \mathbf \Sigma_1^0$, and $\mathbf \Delta_2^0 = \mathbf \Pi_2^0\cap \mathbf \Sigma_2^0$. 

**Def:** For all ordinals $\alpha < \omega_1$ we define the collections of sets of reals $\mathbf \Sigma_\alpha^0$, and $\mathbf \Pi_\alpha^0$ as:
- $$\begin{align*}
{\mathbf \Sigma}_1^0&:= \{B \subseteq \Bbb R \mid B \text{ is open}\} \\
{\mathbf \Pi}_1^0&:= \{B \subseteq \Bbb R \mid B \text{ is closed}\} \\

\end{align*} 
$$
- $$\begin{align*}
  {\mathbf \Sigma}_{\alpha+1}^0 &= \left\{B \subseteq \Bbb R\;\left|\; B = \bigcap_{n \in \Bbb N} B_n,\text{ where each } B_n \in \mathbf \Pi^0_\alpha  \right.\right\}\\
  {\mathbf \Pi}_{\alpha+1}^0 &= \left\{B \subseteq \Bbb R\;\left|\; B = \bigcap_{n \in \Bbb N} B_n,\text{ where each } B_n \in \mathbf \Sigma^0_\alpha  \right.\right\} 
  \end{align*}$$
-  For limit ordinal $\alpha$ $$\begin{align*}
  {\mathbf \Sigma}_{\alpha}^0 &= \left\{B \subseteq \Bbb R\;\left|\; B = \bigcap_{n \in \Bbb N} B_n,\text{ where each } B_n \in \mathbf \Pi^0_\beta \text{ for some } \beta <\alpha  \right.\right\}\\
  {\mathbf \Pi}_{\alpha}^0 &= \left\{B \subseteq \Bbb R\;\left|\; B = \bigcap_{n \in \Bbb N} B_n,\text{ where each } B_n \in \mathbf \Sigma^0_\beta \text{ for some } \beta <\alpha  \right.\right\} 
  \end{align*}$$


**Lemma:** 
- For every $\alpha <\omega_1$, $\mathbf \Sigma_\alpha^0 \subseteq \mathbf \Pi_\alpha^0$ and $\mathbf \Pi_\alpha^0 \subseteq \mathbf \Sigma_\alpha^0$
- For every $\alpha <\omega_1$, $\mathbf \Pi_\alpha^0 \subseteq \mathbf \Pi_\alpha^0$ and $\mathbf \Sigma_\alpha^0 \subseteq \mathbf \Sigma_\alpha^0$
- If $B\in \mathbf \Sigma_\alpha^0$, then $\Bbb R \setminus B \in \mathbf \Pi_\alpha^0$; if $B\in \mathbf \Pi_\alpha^0$, then $\Bbb R \setminus B \in \mathbf \Sigma_\alpha^0$
- If $B_n \in \mathbf \Sigma_\alpha^0$ for each $n \in \Bbb N$, then $\bigcup_{n \in \Bbb N}B_n \in \mathbf \Sigma_\alpha^0$; if $B_n \in \mathbf \Pi_\alpha^0$ for each $n \in \Bbb N$, then $\bigcup_{n \in \Bbb N}B_n \in \mathbf \Pi_\alpha^0$
- If $\alpha < \beta$, then $\mathbf \Sigma_\alpha^0 \subseteq  \mathbf \Sigma_\beta^0$, $\mathbf \Sigma_\alpha^0 \subseteq  \mathbf \Pi_\beta^0$, and $\mathbf \Pi_\alpha^0 \subseteq  \mathbf \Pi_\beta^0$, $\mathbf \Pi_\alpha^0\subseteq  \mathbf \Sigma_\beta^0$ 

**Th:** A set of reals is a Borel set iff it belongs to a $\mathbf \Sigma_\alpha^0$ for some $\alpha<\omega_1$ iff it belongs to $\mathbf \Pi_\alpha^0$ for some $\alpha<\omega_1$

We get that $$\mathcal B = \bigcup_{\alpha < \omega_1} \mathbf \Sigma_\alpha^0 = \bigcup_{\alpha<\omega_1}  \mathbf \Pi_\alpha^0$$
Every uncountable Borel set contains a [[Perfect and Connected Sets in R|perfect subset]]

Let $f: \Bbb R \to \Bbb R$ be a continuous function. If $B \in \mathbf \Sigma_\alpha^0$, then $f^{-1}[B] \in \mathbf \Sigma_\alpha ^0$. Similarly for $\mathbf \Pi_\alpha^0$. 

The cardinality of $\mathcal B$ is $2^{\aleph_0}$.

We can consider the Borel sets to be the closure of countable intersection and union of sets. 