---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Manifolds]], [[Embedded Smooth Submanifolds]], [[Immersed Smooth Submanifolds]], [[Smooth Functions on Smooth Manifolds]], [[The Tangent Bundle]], [[The Cotangent Bundle]]

**Restricting the Domain of a Smooth Map:** If $M$ and $N$ are smooth manifolds with or without a boundary, $F: M \to N$ is a smooth manifold, and $S\subseteq M$ is an immersed or embedded submanifold, then $F|_S : S \to N$ is smooth. 

**Restricting the Codomain of a Smooth Map:** Suppose $M$ is a smooth manifold without boundary, $S\subseteq M$ is an immersed submanifold, and $F: N \to M$ is a smooth map whose image is contained in $S$. If $F$ is a continuous map from $N$ to $S$, then $F:N \to S$ is smooth.

We can strengthen this result using [[Flows and Flowouts on Manifold with Boundary|flows]] to actually drop the requierement that $M$ must be a smooth manifold without a boundary. 

**Restricting the Codomain of a Smooth Map:** Suppose $M$ is a smooth manifold with or without boundary, $S\subseteq M$ is an immersed submanifold, and $F: N \to M$ is a smooth map whose image is contained in $S$. If $F$ is a continuous map from $N$ to $S$, then $F:N \to S$ is smooth.

**Cor:** Suppose $M$ is a smooth manifold without boundary, $S\subseteq M$ is an embedded submanifold. Then every smooth map $F:N \to M$ whose image is contained in $S$ is also a smooth as a map from $N$ to $S$.

**Def:** If $M$ is a smooth manifold and $S\subseteq M$ is an immersed submanifold, then $S$ is said to be *weakly embedded in $M$* if every smooth map $F: N \to M$ whose image lies in $S$ is a smooth map from $N$ to $S$. Weakly embedded submanifolds are also called *initial submanifolds*. 

**Obs:** We see that every embedded submanifold is weakly embedded. 

## Vector and Covector Fields

**Lemma:** Let $M$ be a smooth manifold, and let $S\subseteq M$ be an embedded submanifold, and let $X$ be a smooth vector field on $M$. $Y$ is tangent to $S$ iff $Yf = 0$ on $S$ for every $f\in \mathcal C^\infty (M)$ such that $f|_S  = 0$.

**Prop:** Let $S\subseteq M$ be an immersed submanifold, and let $\iota: S\to M$ denote de inclusion map. If $Y \in \mathfrak X(M)$ is tangent to $S$, then there is a unique smooth vector filed on $S$, denoted by $Y|_S$, that is $\iota$-related to $Y$.

**Cor:** Let $M$ be a smooth manifold and let $S$ be an immersed submanifold. If $Y_1$ and $Y_2$ are smooth vector fields on $M$ that are tangent to $S$, then $[Y_1, Y_2]$ is tangent to $S$ as well.

For covector fields, we only need to consider the pullback of that covector field. 

# Extending Functions from Submanifolds

**Extension Lemma for Functions on Submanifolds:** Suppose $M$ is a smooth submanifold $S\subseteq M$ is a smooth submanifold, and $f\in \mathcal C^\infty(S)$. 
- If $S$ is embedded, then there exists a neighbourhood $U$ of $S$ in $M$ and a smooth function $\tilde f\in \mathcal C^\infty(U)$ such that $\tilde f|_S =f$. 
- If $S$ is properly embedded, then the neighbourhood $U$ form the part above can eb take to be all of $M$. 

**Prop:** Suppose $M$ is a smooth manifold and $S\subseteq M$ is a smooth submanifold. 
- $S$ is embedded if for every $f\in \mathcal C^\infty(S)$ has a smooth extension to a neighbourhood of $S$ in $M$. 
- $S$ is properly embedded if every $f\in\mathcal C^\infty(S)$ has a smooth extension to all of $M$. 
