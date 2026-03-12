---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Space Complexity]], [[The Complexity Class P]], [[The Complexity Class NP]], [[NP-Completeness]], [[Boolean Algebra]]

**Def:** $\sf PSPACE$ is the class of languages that are decidable in polynomial space on a deterministic Turing machine. In other words, $$\mathsf{PSPACE}:= \bigcup_{k \in \Bbb N} \text{SPACE}(n^k). $$Similarly, $\sf NPSPACE$ is the class of lanugages that are decidable in polynomial space on a nondeterministic Turing machine.  $$\mathsf{NPSPACE}:= \bigcup_{k \in \Bbb N} \text{NSPACE}(n^k). $$

**Obs:** By Savitch's Theorem, we know that $\sf PSPACE = NPSPACE$.

We can define $\sf coPSPACE$ to be the class of languages that its complement is in $\sf PSPACE$. Since the deterministic space of complexity classes are closed under complemente, we have that $\sf coPSPACE =PSPACE$. 

For $f(n)\ge n$, a Turing machine that uses $f(n)$ space can have at most $f(n) 2^{O(f(n))}$ different configurations, We summarise our knowledge of the relations among the complexity classes so far in the series of containment $$ \sf P \subseteq NP \subseteq PSPACE = NPSPACE \subseteq EXPTIME.$$

We don't know whether any of these containments is actually an equality. Someone may discover a simulation like the one in Savitch's theorem that merges some of these classes into the same class. 

**Prop:** $\sf PSPACE$ is closed under the operations, union, complementations, and star. 

**Prop:** Let $$EQ_\mathsf{REX} := \{\langle R, S \rangle\mid \text{$R$ and $S$ $\sf REX$s and }L(A) = L(B)\}.$$Then $EQ_\mathsf{REX}\in \sf PSPACE$. 

# $\sf PSPACE$-completeness

**Def:** A language $B$ is $\sf PSPACE$-hard if every $A\in \sf PSPACE$ is polynomial time reducible to $B$. Additionally, We say that $B$ is $\sf PSPACE$-complete if it is both $\sf PSCPACE$-hard, and in $\sf PSPACE$. 

**Obs:** Any $\sf PSPACE$-hard language is also $\sf NP$-hard. 

Complete problems are important because they are examples of the most difficult problems in a complexity class. A complete problem is most difficult because any other problem in the class is easily reduced into it, so if we find an easy way to solve the complete problem, we can easily solve all other problems in the class. The reduction must be *easy*, relative to the complexity of typical problems in the class, for this reasoning to apply. If the reduction itself were difficult to compute, an easy solution to the complete problem wouldn't necessarily yield an easy solution to the problem reducing to it.

Whenever we define complete problems for a complexity class, the reduction model must be more limited than the model used for defining the class itself.

**Obs:** If Every $\sf NP$-hard language is also $\sf PSPACE$-hard, then $\sf PSPACE = NP$.

## The $\text{TQBF}$ Problem

Our first example of a $\sf PSPACE$-complete problem involved a generalisation of the satisfiability problem. A *Boolean formula* is an expression that contains Boolean variables, the constants $0$ and $1$, and the Boolean operators $\land$, $\lor$ and $¬$. 

The *quantifiers* $\forall$ and $\exists$ make frequent appearances in mathematical statements. A quantifier may appear anywhere in a mathematical statement. It applies to the fragment of the statement appearing within the matched pair of parentheses or brackets following the quantified variable. This fragment is called the *scope* of the quantifier. Often, it is convenient to require that all quantifiers appear at the beginning of the statement and that each quantifier's scope is everything following. Such statements are said to be in *prenex normal form*. Any statement may be put into prenex normal form easily. 

Boolean formulas with quantifiers are called *quantified Boolean formulas*. For such formulas, the universe is $\{0, 1\}$. 

When each variable of a formula appears withing the scope of some quantifier, the formula is said to be *fully quantified*. A fully quantified Boolean formula is sometimes called a *sentence* and is always either true or false. 

The $\text{TQBF}$ problem is to determine whether a fully quantified Boolean formula is true or false. We define the language $$\text{TQBF} :=  \{\langle\phi\rangle \mid \text{$\phi$ is a true fully quantified Boolean formula}\}. $$
**Th:** $\text{TQBF}$ is $\sf PSPACE$-complete.

**Prop:** $\text{TQBF}$ restricted to formulas where the part following quantifiers is in conjunctive normal form is still $\sf PSPACE$-complete. 

## Winning Strategies for Games

For the purposes of this small section, a *game* is loosely define to be a competition in which opposing parties  attempt to achieve some goal according to pre-specified rules.

Games are closely related to quantifiers. A quantified statement has a corresponding game; conversely, a game often has corresponding quantified statement. These correspondences are helpful in several ways. For one, expressing a mathematical statement that uses many quantifiers of the corresponding game may give insight into the statement's meaning. For another, expressing a game in terms of a quantified statement aids in understanding the complexity of the game. 

To illustrate the correspondence between games and quantifiers we turn to an artificial game called the *formula game*.

Let $\phi = \exists x_1 \forall x_2 \exists x_3\cdots \mathsf Q x_k [\psi]$ be a quantified Boolean formula in prenex normal form. Here $\sf Q$ represents either a $\forall$ or an $\exists$ quantifier. We associate with $\phi$ as follows. Two players, called player $A$ and player $E$, take turns selecting the values of the variables $x_1,\dots, x_k$. Player $A$ selects values for the variables that are bound to $\forall$ and the player $E$ selects values for the variables that are bound to $\exists$ quantifiers. The order of play is the same as that of the quantifiers of the beginning of the formula. At the end of play we use the values that the players and declare that player $E$ has won the fame if $\psi$, the part of the formula with the quantifiers stripped off, is now true. Player $A$ has won if $\psi$ is false.

A player has a winning strategy for a game if that player wins when both sides play optimally. 

We next consider the problem of determining which player has a winning strategy in the formula game associated with a particular formula. Let $$\text{Formula-Game} := \{\langle \phi\rangle\mid \text{Player $E$ has a winning strategy in the formula game associated with $\phi$}\} $$
**Th:** $\text{Formula-Game}$ is $\sf PSPACE$-complete. We actually see that $\phi\in \text{TQBF}$ exactly when when $\phi\in\text{Formula-Game}$. 

## Generalised Geographies

Now that we know that the formula game is $\sf PSPACE$-complete, we can establish the $\sf PSPACE$-completeness or $\sf PSPACE$-hardness of some other games more easily. We'll begin with a generalisation of the game geography and later discuss games such as chess, checkers, and GO.

Geography is a child's game in which players take turns naming cities from anywhere in the world. Each city chosen must begin with the same letter that ended the previous city's name. Repetition isn't permitted. The game starts with some designated starting city and ends when some player loses because they are unable to continue. 

We can model this game with a directed graph whose nodes are cities of the world. We draw an arrow from one city to another if the first can lead to the second according to the game rules. 

When the rules of geography are interpreted for this graphic representation one player starts by selecting the designated start node and then the players take turns alternatively by picking nodes that form a simple path in the graph. The requirement that the path be simple corresponds to the requirement that a city may not be repeated. The first player unable to extend the path loses the game.

In *generalised geography* we take an arbitrary directed graph with a designated start node instead of the graph associated with the actual cities.

Say that Player $1$ is the one who moves first and Player $2$ second. The problem of determining which player has a winning strategy in a generalised geography game is $\sf PSPACE$-complete. Let$$\text{GG}:= \{\langle G, b\rangle\mid \text{Player $1$ has a winning strategy for the generalised geography game played on graph $G$ starting at node $b$}\}. $$
**Th:** $\text{GG}$ is $\sf PSPACE$-complete.

We showed that no polynomial time algorithm exists for optimal play in generalised geography unless $\sf P = PSPACE$. We'd like to prove a similar theorem regarding the difficulty of computing optimal play in a board games such as chess, but an obstacle arises. Only a finite number of different games positions may occur on the standard $8\times 8$ board. In principle, all these positions may be placed in a table, along with the best move in each position. The table would be too large to fit inside our galaxy, but being finite, could be stored in the control of a Turing machine, or even that of a finite automaton. Thus the machine would be able to play optimally in linear time, using table lookup. Nevertheless, we can give some evidence for the difficulty of computing optimal play for many boards by generalising to an $n \times n$ board. Such generalisations of chess, checkers, and GO have been shown to be $\sf PSPACE$-hard or hard for even larger complexity classes, depending on the details of the generalisation. 