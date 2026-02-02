---
tags:
  - HomologicalAlgebra
---
Subjects: [[Homological Algebra]]
Links: [[Chain Complexes and Cochain Complexes]], [[Exact Sequences]]

**Def:** Suppose $C_\bullet$, $D_\bullet$, and $E_\bullet$ are chain complexes. A sequence of chain maps $$\cdots \stackrel{}{\longrightarrow} C_\bullet \stackrel{F}{\longrightarrow}  D_\bullet\stackrel{G}{\longrightarrow}  E_\bullet \stackrel{}{\longrightarrow} \cdots$$is said to be *exact* if each of the sequences $$\cdots \stackrel{}{\longrightarrow} C_p \stackrel{F}{\longrightarrow}  D_p\stackrel{G}{\longrightarrow}  E_p \stackrel{}{\longrightarrow} \cdots  $$is exact.

**The Zigzag Lemma:** Let $$0 \stackrel{}{\longrightarrow} C_\bullet \stackrel{F}{\longrightarrow}  D_\bullet\stackrel{G}{\longrightarrow}  E_\bullet \stackrel{}{\longrightarrow} 0 $$be a short exact sequence of chain maps. Then for each $p$ there is a connecting homomorphism $\partial_*: H_p(E_\bullet) \to H_{p-1}(C_\bullet)$ such that the following sequence is exact: $$\cdots \stackrel{\partial_*}{\longrightarrow} H_p(C_\bullet) \stackrel{F_*}{\longrightarrow}  H_p(D_\bullet)\stackrel{G_*}{\longrightarrow} H_p( E_\bullet) \stackrel{\partial_*}{\longrightarrow}H_{p-1}(C_\bullet) \stackrel{F_*}{\longrightarrow} \cdots$$The sequence above is called the *long exact homology sequence* associated with the given short exact sequence of chain maps.

**Naturality of the Connecting Homomorphism:** Suppose
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
0\arrow[r] & C_\bullet\arrow[r, "F"]\arrow[d, "\kappa"] & D_\bullet\arrow[r, "G"]\arrow[d, "\delta"] & E_\bullet\arrow[r]\arrow[d, "\varepsilon"] & 0 \\
0\arrow[r] & C_\bullet'\arrow[r, "F'"'] & D_\bullet'\arrow[r, "G'"'] & E_\bullet'\arrow[r] & 0
\end{tikzcd}
\end{document}
```
is a commutative diagram of chain maps in which the horizontal rows are exact. Then the following diagram commutes for each $p$:
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
H_p(E_\bullet) \arrow[d, "\varepsilon_*"']\arrow[r,"\partial_*"] & H_{p-1}(C_\bullet) \arrow[d, "\kappa_*"] \\
H_p(E_\bullet') \arrow[r,"\partial_*"]& H_{p-1}(C_\bullet')
\end{tikzcd}
\end{document}
```

**The Zigzag Lemma:** Given a short exact sequence of cochain complexes$$0 \longrightarrow A^\bullet \stackrel{F}{\longrightarrow} B^\bullet \stackrel{G}{\longrightarrow}  C^\bullet \stackrel{}{\longrightarrow} 0$$ for each $p$ there is a a linear map $$\delta: H^p(C^\bullet) \to H^{p+1}(A^\bullet),  $$called the *connecting homomorphism,* such that the following sequence is exact: $$\cdots \stackrel{\delta}{\longrightarrow}  H^p(A^\bullet) \stackrel{F^*}{\longrightarrow} H^p(B^\bullet) \stackrel{G^*}{\longrightarrow} H^p(C^\bullet) \stackrel{\delta}{\longrightarrow} H^{p+1}(A^\bullet) \stackrel{F^*}{\longrightarrow} \cdots.$$