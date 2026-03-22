---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]], [[Numerical Analysis]]
Links: [[Turing Machines]], [[NP-Completeness]]

In certain problem called *optimisation problems* we seek the best solution among a collection of possible solutions. When an optimisation problem is $\sf NP$-hard. 

In practice, we may not need the absolute best or *optimal* solution to a problem. A solution that is nearly optimal may be good enough and may be much easier to find. As its name implies, an *approximation algorithm* is designed to find such approximately optimal solutions.

If $G$ is an undirected graph a *vertex cover* of $G$ is a subset of nodes where every edge of $G$ touches one of the nodes. The vertex cover problem asks whether a graph contains a vertex cover of a specified size: $$\text{Vertex-Cover}:= \{\langle G, k \rangle \mid \text{$G$ is an undirected graph that has a $k$-node vertex cover}\}. $$
We presented the problem as the language $\text{Vertex-Cover}$ representing a *decision problem,* one that has a yes/no answer. In the optimisation version of this problem, called $\text{Min-Vertex-Cover}$, we aim to produce one of the smallest vertex covers among all possible vertex covers in the input graph. The following polynomial time algorithm approximately solves this optimisation problem. It produces a vertex cover that is never more than twice size of one of the smallest vertex covers.

$A =$"On input $\langle G\rangle$, where $G$ is undirected graph:
1. Repeat the following until all edges in $G$ touch a marked vertex:
	 1. Find an edge in $G$ untouched by any marked edge.
	 2. Mark the edge.
2. Output all nodes that are endpoints of marked edges."

**Th:** $A$ is a polynomial time algorithm that produces a vertex cover of $G$ that is no more than twice as large as smallest vertex cover. 

$\text{Min-Vertex-Cover}$ is an example of a *minimisation problem* because we aim to find the *smallest* among the collection of possible solutions. In a *maximisation problems* we seek the *largest* solution. An approximation algorithm for a minimisation problem is *$k$-optimal* if it always finds a solution that is not more than $k$ times optimal. For a maximisation problem a $k$-optimal approximation algorithm always finds a solution that is at least $\frac{1}{k}$ times the size of the optimal.

We see that $A$ is $2$-optimal for vertex cover problem. 

The following is an approximation algorithm for a maximisation problem called $\text{Max-Cut}$. A *cut* in an undirected graph is a separation of the vertices $V$ into two disjoint subsets $S$ and $T$. A *cut edge* is an edge that goes between the node in $S$ and node in $T$. An *uncut edge* is an edge that is not a cut edge. The size of a cut is the number of cut edges. The $\text{Max-Cut}$ problem asks for a largest cut in a graph $G$. The following algorithm approximates $\text{Max-Cut}$ within a factor of $2$.

$B =$ "On input $\langle G\rangle$ where $G$ is an undirected graph with nodes $V$:
1. Let $S = \varnothing$ and $T= V$.
2. If moving a single node, either from $S$ to $T$ or from $T$ to $S$, increases the size of the cute, make that move and repeat this stage.
3. If no such node exists, output the current cut and halt."

**Th:** $B$ is a polynomial time, $2$-optimal approximation algorithm for $\text{Max-Cut}$.

