---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Time Complexity]], [[The Complexity Class NP]], [[The Complexity Class P]], [[Boolean Equations for Digital Circuits]], [[Boolean Algebra]], [[Graph Colouring]]

**Def:** A function $f:\Sigma^* \to \Sigma^*$ is a *polynomial time computable function* if some polynomial time Turing machine $M$ exists that halts with just $f(w)$ on its tape, when started on any input $w$.

**Def:** Language $A$ is *polynomial time mapping reducible, polynomial time many-one reducibility* or simply *polynomial time reducible*, to language $B$, written $A\le_\text P B$, if a polynomial time function $f:\Sigma^*\to \Sigma^*$ exists, where for every $w$ $$w\in A\iff f(w)\in B.$$The function $f$ is called the *polynomial time reduction* of $A$ to $B$. 

**Th:** If $A\le_\text PB$ and $B\in \sf P$, then $A\in\sf P$.

**Def:** We say that a problem $A$ is *$\sf  NP$-hard* if $A\le_\text P B$ for every $B\in \sf NP$. Similarly, we say that $A$ is $\sf NP$-complete if $A\in \sf NP$ and it is $\sf NP$-hard.

**Obs:** Let $A$ be a an $\sf NP$-complete problem. Let $A\in \sf P$ iff $\sf P = NP$. Also, if $A\le_\text P B$, then that means that $B$ is $\sf NP$-hard. 

**Prop:** If any $A\in \sf P$ is also $\sf NP$-complete, then $\sf P = NP$. 

**Prop:** If $A\in \sf P$, and if we could prove that $A$ is not $\sf NP$-complete, then $\sf P \neq NP$. 

# SAT

A *Boolean formula* is an expression involving Boolean variables and operations. A boolean formula is *satisfiable* if some assignment of $0$s and $1$s to the variables make the formula to evaluate $1$. We say that the assignment *satisfies* the Bolean formula $\phi$. The *satifiabiliy problem* is to test whether a Boolean formula is satisfiable. Let $$\text{SAT}:= \{\langle\phi\rangle\mid \text{$\phi$ is a satisfiable Boolean formula}\}.$$
We also care about an important variation of the $\text{SAT}$ problem called $3\text{SAT}$, a special case of the satifiability problem whereby all formulas are in a special form. A *literal* is a Boolean variable or a negated Boolean variable, as in $x$ or $\overline $x$. A *clause* is several literals connected with $\lor$s. A Bolean formula is in *conjuntive normal form*, called a *cnf-formula*, if it comprises several clauses connected with $\land$s. It is a $3$cnf-formula if all clauses have three literals. Let $$3\text{SAT}:= \{\langle\phi\rangle\mid \text{$\phi$ is a satisfiable 3cnf-formula formula}\}.$$In a satisfiable cnf-formula each clause must contain at least one literal that is assigned $1$. 

**Th:** $3\text{SAT}$ is polynomial time reducible to $\text{Clique}$, see [[The Complexity Class NP#Examples of $ sf NP$-problems|here]] for definition of $\text{Clique}$. 

Using the notion of completeness that naturally arose when studying the [[Oracle Machines and Relative Computation#Arithmetic Hierarchy|Arithmetic hierarchy]], we can study similar problems whose individual complexity is related to that of the entire class. If a polynomial time algorithm exists for any of these problems, all problems in $\sf NP$ would be polynomial time solvable. These problems are *$\sf NP$-complete.*

**Cook-Levin Theorem:** $\text{SAT}$ is an $\sf NP$-complete problem.

**Cor:** $3\text{SAT}$ is $\sf NP$-complete.

Sketch of the Cook-Levin:

We take any language $A$ in $\sf NP$ and show that $A$ is polynomial time reducible to $\text{SAT}$. Let $N$ be a nondeterministic Turing machine that decides $A$ in $n^k-3$ for some constant $k$. We consider a *tableau* for $N$ on  $w$ is an $n^k\times n^k$ table whose rows are the configuration of a branch of the computation of $N$ on input $w$. 

Each configuration starts and ends with a $\#$ symbol, so the first and last columns of a tableau are all $\#$s. The first row of a tableua is the starting configuration of $N$ on $w$, and each row follows previous one according to $N$'s transition function. A tableau is *accepting* if any row of the tableau is an accepting configuration.

On input $w$, the wanted polynomial reduction produces a formula $\phi$. We begin describing the variables of $\phi$. Say that $Q$ and $\Gamma$ are the state set and the tape alphabet of $N$. Let $C := Q \cup \Gamma\cup\{\#\}$. For each $i$ and $j$ between the $1$ and $n^k$ and for each $s\in S$ we have a variable $x_{i, j,s}$. 

Each of the $(n^k)^2$ entries of a tableau is called a *cell*. The cell in row $i$ and column $j$ is called $\text{cell}[i, j]$, and contains a symbol from $C$. If $x_{i, j, s}$ takes on the value of $1$, it means that $\text{cell}[i, j]$ contains $s$. 

We want to break $\phi$ into four parts: $\phi_\text{cell}, \phi_\text{start}, \phi_\text{move}$, and $\phi_\text{accept}$. 

We want to ensure a correspondence between an assignment and a tableau is that assigment turns on exactly one variable for each cell. Thus we mustt have the following definition$$\phi_\text{cell} := \bigwedge_{1\le i, j\le n^k} \left[\left(\bigvee_{s\in S}x_{i, j, s}\right) \land \left(\bigvee_{\substack{s\in S \\ s\neq t}}\overline{x_{i, j, s}} \lor \overline{x_{i, j, t}}\right) \right].  $$
Formula for $\phi_\text{start}$ ensures that the first row of the table is starting configuration of $N$ on $w$ by explicitly stipulating that the corresponding variables are on: $$\phi_\text{start} := x_{1, 1, \#} \land x_{i, 2, q_0}\land  \left(\bigwedge_{i = 3}^{n+2}x_{1, i, w_i}\right) \land \left(\bigwedge_{i = n+3}^{n^k-1}x_{1, i, \textvisiblespace}\right) \land  x_{1, n^k, \#}.$$
The formula $\phi_{accept}$ guarantees than an accepting configuration occurs in the tableau. It ensures that $q_\text{accept}$, the symbol for the accept state, appears in one of the cells of the tableau. $$\phi_\text{accept} := \bigvee_{1\le i, j\le n} x_{i, j, q_\text{accept}}.$$
Finally, formula $\phi_\text{move}$ guarantees that each row of the table corresponds to a configuration that legally follows the preceding row's configuration according to $N$'s rules. It does so by ensuring that each $2\times 3$ window of cells is legal . The precises definition of *legal window* can be a little tedious, and it is similar to the construction to the proof related to the [[Post Systems|Post Correspondence Problem]]. 

**Claim:** If the top row of the start configuration and every window in the table is legal, each row of the table is a configuration that legally follows the preceding one. 

Now we return to the construction of $\phi_\text{move}$. It stipulates that all the windows in the tableau are legal. Each window contains six cells, which may be set in a fixed number of ways to yield a legal window.  $$\phi_\text{move}:= \bigwedge_{\substack{1\le i < n^k \\ 1< j<n^k}} \bigvee_{\substack{a_1,\dots, a_6 \\ \text{is a legal window}}} (x_{i, j-1, a_1}\land x_{i, j, a_2}\land x_{i, j+1, a_3}\land x_{i, j-1, a_4}\land x_{i, j, a_5}\land x_{i, j+1, a_6}). $$Our final formula is $$\phi:= \phi_\text{cell}\land \phi_\text{start} \land \phi_\text{accept} \land \phi_\text{move}.$$The reduction made is in the order of $O(n^{2k} \log n)$ so it is still a polynomial reduction, since we can consider it a $O(n^{2k+1})$. 

# Additional $\sf NP$-complete Problems

**Cor:** $\text{Clique}$ is $\sf NP$-complete.

If $G$ is an undirected graph a *vertex cover* of $G$ is a subset of nodes where every edge of $G$ touches one of the nodes. The vertex cover problem asks whether a graph contains a vertex cover of a specified size: $$\text{Vertex-Cover}:= \{\langle G, k \rangle \mid \text{$G$ is an undirected graph that has a $k$-node vertex cover}\}. $$
**Th:** $\text{Vertex-Cover}$ is $\sf NP$-complete. 

**Th:** $\text{HamPath}$ is $\sf NP$-complete.

**Th:** If $\text{UHampPath}$ represents is the problem of a Hamiltonian path in an undirected graph. the $\text{UHamPath}$ is $\sf NP$-complete. 

**Th:** $\text{Subset-Sum}$ is $\sf NP$-complete. 

**Prop:** Let $\text{LPath}:= \{\langle G, a, b, k\rangle \mid G \text{ contains a simple path of length at least }k\text{ from }a \text{ to  }b\}$. Then $\text{LPath}$ is $\sf NP$-complete.

**Prop:** Let $$\text{Double-SAT}:= \{\langle \phi\rangle\mid \phi \text{ has at least two satisfying assigments}\}.$$Then $\text{Double-SAT}$ is $\sf NP$-complete. 

**Prop:** Let $$\text{Half-Clique} := \{\langle G\rangle \mid G \text{ is an undirected graph having a complete graph with at least }m/2 \text{ nodes, where $m$ is the number of nodes in }G\}.$$Then $\text{Half-Clique}$ is $\sf NP$-complete. 

Let $\text{CNF}_k := \{\langle \phi \rangle \mid \phi \text{ is a satisfiable cnf-formula where each variable appears in at most }k \text{ places}\}.$
**Prop:** $\text{CNF}_3$ is $\sf NP$-complete.

Let $\phi$ be a $3$cnf-formula. An *$\ne$-assignment* to the variables of $\phi$ is one where each clause contains two literals unequal truth values. In other words, an $\ne$-assignment satisfies $\phi$ without assigning three true literals in any clause.

**Obs:** The negation of any $\ne$-assignment to $\phi$ is also an $\neq$-assignment. 

Let $\neq\text{SAT}$ or $\text{NAE-SAT}$ be the collection of $3$cnf-formulas that have an $\neq$-assignment. 

**Prop:** $\neq\text{SAT}$ is $\sf NP$-complete. 

A *cut* in an undirected graph is a separation of vertices $V$ into two disjoint subsets $S$ and $T.$ The size of the cute is the number of edges that have one endpoint in $S$ and the other in $T$. Let  $$\text{Max-Cut} := \{\langle G, k \mid \text{$G$ has a cut of size $k$ or more}\}. $$
**Prop:** $\text{Max-Cut}$ is $\sf NP$-complete.

**Prop:** Let $3\text{Color} := \{\langle G\rangle \mid G \text{ is an undirected graph that can be coloured with only }3\text{ colours}\}$. Then $3\text{Color}$ is $\sf NP$-complete. 

**Prop:** Let $$\begin{align*}
\text{Set-Splitting} := &\{\langle S, C\rangle \mid S \text{ is a fintie set and } C := \{C_1,\dots, C_k\}\subseteq \mathcal P(S), \\&\text{ for some }k> 0, \text{ such that elements of $S$ can be colored red or blue }\\& \text{so that no $C_i$ has all its elements colored with the same colors} \}.\end{align*}$$
Then $\text{Set-Splitting}$ is $\sf NP$-complete. 

**Prop:** Let $U := \{\langle M, x, \#^t\rangle \mid \mathsf{TM} M \ŧex}