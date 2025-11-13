---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]]

**Def:** Two field extensions $L/F$ and $K/k$ are *isomorphic* is there exists a pair of field isomorphisms $\phi: L \to K$ and $\psi: F \to k$ such that the following diagram commutes 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]    
L\arrow[r, "\phi"]\arrow[d, dash] & K\arrow[d, dash]\\
F\arrow[r, "\psi"] & k
\end{tikzcd}
\end{document}
```
meaning, $\phi|_F = \psi$. 

**Def:** An *isomorphism* between two extension $L/F$ and $K/F$ over the same field, is an field isomorphism $\phi: L \to K$ such that $\phi|_F = \text{id}_F$