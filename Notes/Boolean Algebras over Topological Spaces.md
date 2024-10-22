---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Lattices]], [[Regular Open and Closed Sets]], [[Topological Spaces]]

We have that the set of all clopen sets of $X$, with the partial order $\subseteq$, and the operations of union, intersection, and complement, with the distinguished elements $X$ and $\varnothing$, for a boolean algebra

The collection ${\cal RO}(X)$ of regular open sets forms a Boolean algebra when we consider the operations $A \wedge B = \inf\{A, B\} = A\cap B$, and $A\lor B = \sup\{A, B\} = \text{int}(\text{cl}(A\cup B))$, and for every $A \in {\cal RO}(X)$, we define $A'= X\setminus \text{cl}(A)$, and the distinguished elements are $0 = \varnothing$ and $1 = X$  

The collection ${\cal RC}(X)$ of regular closed sets forms a Boolean algebra when we consider the operations $A \wedge B = \inf\{A, B\} = \text{cl}(\text{int} (A\cap B))$, and $A\lor B = \sup\{A, B\} = A\cup B$, and for every $A \in {\cal RO}(X)$, we define $A'= X\setminus \text{int}(A)$, and the distinguished elements are $0 = \varnothing$ and $1 = X$  