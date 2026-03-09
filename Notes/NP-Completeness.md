---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Time Complexity]], [[The Complexity Class NP]], [[The Complexity Class P]], [[Boolean Equations for Digital Circuits]], [[Boolean Algebra]]

**Def:** A function $f:\Sigma^* \to \Sigma^*$ is a *polynomial time computable function* if some polynomial time Turing machine $M$ exists that halts with just $f(w)$ on its tape, when started on any input $w$.

**Def:** Language $A$ is *polynomial time mapping reducible, polynomial time many-one reducibility* or simply *polynomial time reducible*, to language $B$, written $A\le_\text P B$, if a polynomial time function $f:\Sigma^*\to \Sigma^*$ exists, where for every $w$ $$w\in A\iff f(w)\in B.$$The function $f$ is called the *polynomial time reduction* of $A$ to $B$. 

**Th:** If $A\le_\text PB$ and $B\in \sf P$, then $A\in\sf P$.

# SAT

A *Boolean formula* is an expression involving Boolean variables and operations. A boolean formula is *satisfiable* if some assignment of $0$s and $1$s to the variables make the formula to evaluate $1$. We say that the assignment *satisfies* the Bolean formula $\phi$. The *satifiabiliy problem* is to test whether a Boolean formula is satisfiable. Let $$\text{SAT}:= \{\langle\phi\rangle\mid \text{$\phi$ is a satisfiable Boolean formula}\}.$$
We also care about an important variation of the $\text{SAT}$ problem called $3\text{SAT}$, a special case of the satifiability problem whereby all formulas are in a special form. A *literal* is a Boolean variable or a negated Boolean variable, as in $x$ or $\overline $x$. A *clause* is several literals connected with $\lor$s. A Bolean formula is in *conjuntive normal form*, called a *cnf-formula*, if it comprises several clauses connected with $\land$s. It is a $3$cnf-formula if all clauses have three literals. Let $$3\text{SAT}:= \{\langle\phi\rangle\mid \text{$\phi$ is a satisfiable 3cnf-formula formula}\}.$$In a satisfiable cnf-formula each clause must contain at least one literal that is assigned $1$. 

**Th:** $3\text{SAT}$ is polynomial time reducible to $\text{Clique}$, see [[The Complexity Class NP#Examples of $ sf NP$-problems|here]] for definition of $\text{Clique}$. 

Using the notion of completeness that naturally arose when studying the [[Oracle Machines and Relative Computation#Arithmetic Hierarchy|Arithmetic hierarchy]], we can study similar problems whose individual complexity is related to that of the entire class. If a polynomial time algorithm exists for any of these problems, all problems in $\sf NP$ would be polynomial time solvable. These problems are *$\sf NP$-complete.*

**Def:** We say that a problem $A$ is *$\sf  NP$-hard* if $A\le_\text P B$ for every $B\in \sf NP$. Similarly, we say that $A$ is $\sf NP$-complete if $A\in \sf NP$ and it is $\sf NP$-hard.

**Obs:** Let $A$ be a an $\sf NP$-complete problem. Let $A\in \sf P$ iff $\sf P = NP$.

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



# Additional $\sf NP$-complete Problems

**Cor:** $\text{Clique}$ is $\sf NP$-complete.