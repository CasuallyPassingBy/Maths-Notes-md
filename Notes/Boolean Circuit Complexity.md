---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]], [[Digital Circuits]]
Links: [[The Complexity Class NP]], [[NP-Completeness]], [[Turing Machines]]

Computers are built from electronic devices wired together in a design called a *digital circuit*. We can also simulate theoretical models with the theoretical counter part to digital circuits, called *Boolean circuits*. Two purposes are served by establishing the connection between Turing machines and Boolean circuits. First, researchers believe that circuits provide a convenient computational model for attacking $\sf P$ vs $\sf NP$ and related questions. Second, circuits provide an alternative proof of the Cook-Levin theorem that $\text{SAT}$ is $\sf NP$-complete.

**Def:** A *Boolean circuits* is a collection of *gates* and *inputs* connected by *wires*. Cycles aren't permitted. Gates take three forms: $\text{AND}$ gates, $\text{OR}$ ages, and $\text{NOT}$ gates. This can be shown diagramatically as in the following figure. 
```tikz
\usepackage{tikz}
\usetikzlibrary{positioning}

\begin{document}

\begin{tikzpicture}[
    % Global styles for the nodes and lines
    gate/.style={draw, circle, minimum size=0.8cm, inner sep=0pt},
    line/.style={draw, -}
]

    % --- AND GATE ---
    \node[gate] (and) at (0,0) {$\wedge$};
    \node[below=0.1cm of and] {AND};
    % Inputs
    \draw (and.120) -- ++(120:0.5cm);
    \draw (and.60) -- ++(60:0.5cm);
    % Output
    \draw (and.270) -- ++(270:0.5cm);

    % --- OR GATE ---
    \node[gate] (or) at (2.5,0) {$\vee$};
    \node[below=0.1cm of or] {OR};
    % Inputs
    \draw (or.120) -- ++(120:0.5cm);
    \draw (or.60) -- ++(60:0.5cm);
    % Output
    \draw (or.270) -- ++(270:0.5cm);

    % --- NOT GATE ---
    \node[gate] (not) at (5,0) {$\neg$};
    \node[below=0.1cm of not] {NOT};
    % Input
    \draw (not.90) -- ++(90:0.5cm) node[right=0.2cm, black]{};
    % Output
    \draw (not.270) -- ++(270:0.5cm) node[right=0.2cm, black]{};

\end{tikzpicture}

\end{document}
```

The wires in a Boolean circuit carry the Boolean values $0$ and $1$. The gates are simple processors that compute the Boolean functions $\text{AND}, \text{OR}$, and $\text{NOT}$. The $\text{AND}$ function outputs $1$ if both of its input are $1$ and outputs $0$ otherwise. The $\text{OR}$ function outputs $0$ if both of its inputs are $0$ and outputs $1$ otherwise. The $\text{NOT}$ function outputs the opposite of its input. The inputs are labelled $x_1,\dots, x_n$. One of the gates is designates the *output gate*. 

A Boolean circuit computes an output value from setting of the inputs by propagating values along the wires and computing the function associated with the respective gates until the output gate is assigned a value. The following figure shows a Boolean circuit computing a value from a setting of its input.

We use functions to describe the input/output behaviour of Boolean circuits. To a Boolean circuit $C$ with $n$ inputs variables, we associate a function $f_C:\{0, 1\}^n\to\{0, 1\}$, where if $C$ outputs $b$ when its inputs $x_1,\dots,x_n$ are set to $a_1, \dots, a_n$, we write $f_C(a_1,\dots, a_n) = b$. We say that $C$ computes the function $f_C$. We sometimes consider Boolean circuits that have multiple output gates. A function with $k$ outputs bits computes a function whose range $\{0, 1\}^k$. 

We plan to use circuits to test membership in languages, once they have been suitably encoded into $\{0, 1\}$. One problem that occurs is that any particular circuit can handle all inputs of some fixed length, where as a language may contain strings of different lengths.

**Def:** A *circuit family* $C$ is an infinite sequence of circuits $(C_0, C_1, C_2, \dots, ),$ where $C_n$ has $n$ input variables. We say that $C$ decides a language $A$ over $\{0, 1\}$ if, for every string $w,$  $$w\in A \iff C_n(w) = 1, $$where $n$ is the length of $w$.

The *size* of a circuit is the number of gates that it contains. Two circuits are equivalent if they have the same input variables and output the same value of on every input assignment. A circuit is *size minimal* if no smaller circuit is equivalent to it. The problem of minimising circuits has obvious engineering application but it is very difficult to solve in general. Even testing whether a particular circuit is minimal does not appear to be solvable in $\sf P$ or in $\sf NP$. A circuit family for a language is minimal if every $C_i$ on the list is a minimal circuit. The *size complexity* of a circuit family $(C_0, C_1, C_2, \dots)$ is the function $f:\Bbb N \to \Bbb N$, where $f(n)$ is the size of $C_n$.

The *depth* of a circuit is the length of the longest path from an input variable to the output gate. We define *depth minimal* circuits and circuit families, and the *depth complexity* of circuit families, as we did with circuit size. 

**Def:** The *circuit size complexity* of a language is the size complexity of a minimal circuit family for that language. The *circuit depth complexity* of a language is defined similarly, using depth instead of size.

**Th:** Let $t:\Bbb N \to \Bbb N$ be a function, where $t(n) \ge n$. If $A\in \text{TIME}(t(n))$, then $A$ has circuit complexity $O(t(n)^2)$.

We say that Boolean circuit is *satisfiable* if some setting of the inputs causes the circuit to output $1$. The *circuit-satisfiability* problem tests whether a circuit is satisfiable. Let $$\text{Circuit-SAT} := \{\langle C \rangle \mid \text{$C$ is a satisfiable Boolean circuit}\}. $$
**Th:** $\text{Circuit-SAT}$ is $\sf NP$-complete.

**Cook-Levin Theorem:** $3\text{SAT}$ is $\sf NP$-complete.

**Prop:** We define the parity function $\text{parity}_n$ outputs $1$ if an odd number of $1$s appear in the input variables. Then $\text{parity}_n$ can be computed with $O(n)$ size circuits. 

**Prop:** Let $\text{add}_n: \{0, 1\}^{2n} \to\{0, 1\}^{n+1}$ take the sum of two $n$ bit binary integers and produce the $n+1$ bit result. Then we can compute the $\text{add}_n$ function with $O(n)$ size circuit.