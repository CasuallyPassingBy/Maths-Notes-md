---
tags:
  - DigitalCircuits
---
Subjects: [[Digital Circuits]]

*Logic gates* are simple digital circuits that take one or more binary inputs and produce a binary output. Logic gates are down with a symbol showing the input(s) and the output. Inputs are usually drawn on the left, or top, and outputs on the right (or bottom). Digital Designers typically use letters near the beginning of the alphabet for gate inputs and the output can be described with a truth table or Boolean equation.
### $\text{NOT}$ Gate
A $\text{NOT}$ *gate* has one input $A$, and one output $Y$. The $\text{NOT}$ gate's output is inverse of its input. We will use the notation $Y= \overline A$, and it is read as $Y$ is equal to *not* $A$, other notations are in use such that $~\lnot A$, $A'$, $!A$, or $\sim A$. 

```tikz
\usetikzlibrary{arrows, shapes.gates.logic.US, calc}

\begin{document}
\begin{tikzpicture}
    \node (A) at (0,0) {$A$};

    % NOT gate
    \node[not gate US, draw, logic gate inputs=nn] (notA) at (1.2,0) {};

    % Wiring
    \draw (A) -- (notA.input);
    \draw (notA.output) -- ++(1,0) node[right]{$Y$};
\end{tikzpicture}
\end{document}
```
And the logic table is  

| A   | Y   |
| --- | --- |
| 0   | 1   |
| 1   | 0   |

### Buffer
The other one-input logic is called a *buffer*. It simply copies the input to the output. 

```tikz
\usetikzlibrary{arrows, shapes.gates.logic.US, calc}

\begin{document}
\begin{tikzpicture}
    \node (A) at (0,0) {$A$};

    % NOT gate
    \node[buffer gate US, draw, logic gate inputs=nn] (notA) at (1.2,0) {};

    % Wiring
    \draw (A) -- (notA.input);
    \draw (notA.output) -- ++(1,0) node[right]{$Y$};
\end{tikzpicture}
\end{document}
```
and the logic table is 

| A   | Y   |
| --- | --- |
| 0   | 0   |
| 1   | 1   |

From the logical point of view, a buffer is no different from a wire, so it might seem useless. However, from the analogue point of view, the buffer might have desirable characteristics. The triangle symbol indicates a buffer. A circle on the output is called a *bubble* and indicates inversion, as was seen in the $\text{NOT}$ gate symbol. 

### $\text{AND}$ Gate
Two-input logic gates are more interesting. The $\text{AND}$ *gate* produces a $\text{TRUE}$ output $Y$, if and only if, both $A$ and $B$ are $\text{TRUE}$. Otherwise the output is $\text{FALSE}$. The Boolean equation for an $\text{AND}$ gate can be written in several ways: $Y = A \cdot B$, $Y = A B$, or $Y = A\cap B$. We prefer $Y = AB$. 

```tikz
\usetikzlibrary{arrows, shapes.gates.logic.US, calc}

\begin{document}
\begin{tikzpicture}
    \node (A) at (0,0.5) {$A$};
    \node (B) at (0,-0.5) {$B$};

    % AND gate
    \node[and gate US, draw, logic gate inputs=nn] (and1) at (1.4,0) {};

    % Wiring
    \draw (A) |- (and1.input 1);
    \draw (B) |- (and1.input 2);

    \draw (and1.output) -- ++(1,0) node[right] {$Y$};
\end{tikzpicture}
\end{document}

```
and the logic table is

| A   | B   | Y   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   |

### $\text{OR}$ Gate
The $\text{OR}$ *gate* produces a $\text{TRUE}$ output $Y$, if either $A$ or $B$ are $\text{TRUE}$. The Boolean equation for an $\text{OR}$ gate is written as $Y= A+ B$ or $Y = A\cup B$. 

```tikz
\usetikzlibrary{arrows, shapes.gates.logic.US, calc}

\begin{document}
\begin{tikzpicture}
    \node (A) at (0,0.5) {$A$};
    \node (B) at (0,-0.5) {$B$};

    % AND gate
    \node[or gate US, draw, logic gate inputs=nn] (and1) at (1.4,0) {};

    % Wiring
    \draw (A) |- (and1.input 1);
    \draw (B) |- (and1.input 2);

    \draw (and1.output) -- ++(1,0) node[right] {$Y$};
\end{tikzpicture}
\end{document}

```
and the logic table is

| A   | B   | Y   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 1   |

### $\text{XOR}$ Gate

he $\text{XOR}$ *gate* produces a $\text{TRUE}$ output $Y$, if either $A$ or $B$, but not both, are $\text{TRUE}$. The Boolean equation for an $\text{OR}$ gate is written as $Y= A\oplus B$ or $Y = A\cup B$. 

```tikz
\usetikzlibrary{arrows, shapes.gates.logic.US, calc}

\begin{document}
\begin{tikzpicture}
    \node (A) at (0,0.5) {$A$};
    \node (B) at (0,-0.5) {$B$};

    % AND gate
    \node[xor gate US, draw, logic gate inputs=nn] (and1) at (1.4,0) {};

    % Wiring
    \draw (A) |- (and1.input 1);
    \draw (B) |- (and1.input 2);

    \draw (and1.output) -- ++(1,0) node[right] {$Y$};
\end{tikzpicture}
\end{document}

```
and the logic table is

| A   | B   | Y   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 0   |

### $\text{N}$ Gates
Any gate can be followed by a bubble to invert its operation. The $\text{NAND}$ *gate* performs $\text{NOT AND}$. Its output is $\text{TRUE}$ unless both inputs are $\text{TRUE}$. The $\text{NOR}$ *gate* performs $\text{NOT OR}$. Its output is $\text{TRUE}$ if neither $A$ nor $B$ is $\text{TRUE}$. The $\text{XNOR}$ gate performs $\text{NOT XOR}$. Its output is $\text{TRUE}$ if and only if both its inputs are the same. For this reason, the two input $\text{XNOR}$ gate is sometimes called an *equality*. They have the following truth tables. 

| A   | B   | NAND | NOR | XNOR |
| --- | --- | ---- | --- | ---- |
| 0   | 0   | 1    | 1   | 1    |
| 0   | 1   | 1    | 0   | 0    |
| 1   | 0   | 1    | 0   | 0    |
| 1   | 1   | 0    | 0   | 1    |
```tikz
\usetikzlibrary{arrows, shapes.gates.logic.US, calc}

\begin{document}
\begin{tikzpicture}[circuit/.style={draw, logic gate inputs=nn}]

    % ==== NAND ====
    \node (A1) at (0,2.0) {$A$};
    \node (B1) at (0,1.0) {$B$};
    \node[nand gate US, circuit] (nand1) at (2,1.5) {};
    \draw (A1) |- (nand1.input 1);
    \draw (B1) |- (nand1.input 2);
    \draw (nand1.output) -- ++(1,0) node[right]{$A \uparrow B$};


    % ==== NOR ====
    \node (A2) at (0,0) {$A$};
    \node (B2) at (0,-1.0) {$B$};
    \node[nor gate US, circuit] (nor1) at (2,-0.5) {};
    \draw (A2) |- (nor1.input 1);
    \draw (B2) |- (nor1.input 2);
    \draw (nor1.output) -- ++(1,0) node[right]{$A \downarrow B$};


    % ==== XNOR ====
    \node (A3) at (0,-3.0) {$A$};
    \node (B3) at (0,-4.0) {$B$};
    \node[xnor gate US, circuit] (xnor1) at (2,-3.5) {};
    \draw (A3) |- (xnor1.input 1);
    \draw (B3) |- (xnor1.input 2);
    \draw (xnor1.output) -- ++(1,0) node[right]{$A \odot B$};

\end{tikzpicture}
\end{document}


```

## $N$ inputs Logic Gates
An $N$-input $\text{AND}$ produces $\text{TRUE}$ output when all $N$ inputs are $\text{TRUE}$. An $N$-input $\text{OR}$ gates produces $\text{TRUE}$ output when at least one input is $\text{TRUE}$. An $N$-input $\text{XOR}$ gate is sometimes called a *parity gate* and produces $\text{TRUE}$ output if an odd number of inputs are $\text{TRUE}$. As with two-input gates, the input combinations in the 