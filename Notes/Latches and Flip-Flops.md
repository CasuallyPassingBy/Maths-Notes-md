---
tags:
  - DigitalCircuits
---
Subjects: [[Digital Circuits]]
Links: [[Logic Gates]]

The fundamental building block of memory is a *bistable element*, an element with two stable elements. Stable and elements such as latches and flip-flops provide inputs to control the value.

## S-R Latch
One of the simplest sequential circuits is the  *SR latch*, which is composed of two crossed coupled $\text{NOR}$ gates. 
```tikz

\usepackage{tikz}
\usetikzlibrary{circuits.logic.US}
\tikzstyle{branch}=[fill,shape=circle,minimum size=2pt,inner sep=0pt]

\def\srdefaultlength{0.5cm}
\begin{document}
\begin{tikzpicture}[circuit logic US, node distance=2cm]

    % Gates
    \node[nor gate, inputs=nn] (n1) at (0,0) {};
    \node[nor gate, inputs=nn, below of=n1] (n2) {};

    % Input terminals
    \draw (n1.input 1) --++(-2*\srdefaultlength,0) node[left] {$S$};
    \draw (n2.input 2) --++(-2*\srdefaultlength,0) node[left] {$R$};

    % Feedback inputs
    \draw (n1.input 2) --++(-\srdefaultlength,0) --++(0,-\srdefaultlength) coordinate (tmp1);
    \draw (n2.input 1) --++(-\srdefaultlength,0) --++(0,\srdefaultlength) coordinate (tmp2);

    % Feedback outputs
    \draw (n1.output) --++(\srdefaultlength,0) node[branch](tmp3){}; 
    \draw (tmp3) --++(0,-\srdefaultlength) -- (tmp2);
    \draw (n2.output) --++(\srdefaultlength,0) node[branch](tmp4){}; 
    \draw (tmp4) --++(0,\srdefaultlength) -- (tmp1);

    % Output terminals
    \draw (tmp3) --++(\srdefaultlength,0) node[right] {$Q$};
    \draw (tmp4) --++(\srdefaultlength,0) node[right] {$\overline{Q}$};

\end{tikzpicture} 
\end{document}
```

The latch has two inputs, $S$ and $R$, and two outputs $Q$ and $\overline Q$. The SR latch it can be controlled through the inputs $S$ and $R$, which are *set* and *reset* the output $Q$.

A good way to understand an unfamiliar circuit is to work out its truth table, so that is where we begin. 
- If $R = 1$, $S = 0$, we see that $Q = 0$, and $\overline Q = 1$.
- If $R = 0$, $S = 1$, we see that $\overline Q = 0$, and $Q = 1$.
- If $R = 1$, $S = 1$, we see that $Q = 1$, and $\overline Q = 1$.
- If $R= 0$, $S = 0$, we must check subcases:
	- If $Q = 0$, then $\overline Q = 1$. 
	- If $Q = 1$, then $\overline Q = 0$. 
Putting this all together, suppose $Q$ has some known prior value which we will call $Q_\text{prev}$, before we enter the last case. $Q_\text{prev}$ is either $0$ or $1$, and represents the state of the system. When $R$ and $S$ are $0$, $Q$ will remeber this old value $Q_\text{prev}$, and $\overline Q$ will be its complement $\overline{Q_\text{prev}}$. This circuit has memory. We can see that in the truth table. 

| $S$ | $R$ | $Q$             | $\overline Q$              |
| --- | --- | --------------- | -------------------------- |
| 0   | 0   | $Q_\text{prev}$ | $\overline{Q_\text{prev}}$ |
| 0   | 1   | 0               | 1                          |
| 1   | 0   | 1               | 0                          |
| 1   | 1   | 0               | 0                          |

The inputs $S$ and $R$ stand for *set* and *reset*. To *set*a bit means to make it $\text{TRUE}$. To *reset* a bit is to make it $\text{FALSE}$. The outputs $Q$ and $\overline Q$, are normally complementary. When $R$ is asserted, $Q$ is reset to $0$ and $\overline Q$ does the opposite. When $S$ is asserted, $Q$ is set to $1$ and $\overline Q$ does the opposite. When neither input is asserted, $Q$ remembers its old value, $Q_\text{prev}$. Asserting both $S$ and $R$ simultaneously doesn't make much sense it means the latch should be set and reset at the same time which is impossible.

The SR latch is a bistable element which one bit of state is stored in $Q$. However, the state can be controlled through $S$ and $R$ inputs. 

```tikz
\begin{document}
\begin{tikzpicture}[thick]
    % Box
    \node[draw, minimum width=2.5cm, minimum height=2cm] (box) {};

    % Label
    \node at (box) {\textbf{SR}};

    % Inputs
    \draw (box.west |- 0,0.4) -- ++(-1,0) node[left] {$S$};
    \draw (box.west |- 0,-0.4) -- ++(-1,0) node[left] {$R$};

    % Outputs
    \draw (box.east |- 0,0.4) -- ++(1,0) node[right] {$Q$};
    \draw (box.east |- 0,-0.4) -- ++(1,0) node[right] {$\overline{Q}$};

\end{tikzpicture}
\end{document}
```
## D Latch
The SR lath is awkward because it behaves strangely when both $S$ and $R$ are simultaneously asserted. Moreover, the $S$ and $R$ conflate the issues of *what* and *when*. Asserting one of the inputs determines the issued of *what* the state should be but also *when* it should change. The D latch solve these problems. It has two inputs. The *data* input $D$, controls what the next state should be. The *clock input* $\text{CLK}$, controls when the state should change.

```tikz
\usepackage{tikz}
\usetikzlibrary{circuits.logic.US}

\begin{document}

\begin{tikzpicture}[circuit logic US, thick, node distance=1.8cm]

    % Inputs
    \node (CLK) at (0,1) {CLK};
    \node (D)   at (0,-1) {D};

    % CLK vertical branch
    \draw (CLK) -- ++(0.8,0) coordinate(clkright);
    \draw (clkright) |- ++(0,-2) coordinate(clkdown);

    % Inverter for D'
    \node[not gate US, draw, scale=1] (not1) at (2,-0.2) {};

    % Upper AND (generates R)
    \node[and gate US, draw, scale=1, logic gate inputs=nn] (andR) at (4,0.7) {};

    % Lower AND (generates S)
    \node[and gate US, draw, scale=1, logic gate inputs=nn] (andS) at (4,-1.2) {};

    % SR latch on the right (as a box)
    \draw (5.8,1.2) rectangle (7.6,-1.7);

    % SR labels
    \node at (5.9,0.6) {R};
    \node at (5.9,-0.9){S};

    % Q, Qbar labels
    \node at (7.4,0.6)  {$Q$};
    \node at (7.4,-0.9) {$\overline{Q}$};

    % Wiring: D to NOT gate
    \draw (D) -- ++(1.3,0) |- (not1.input);

    % NOT output to upper AND (R)
    \draw (not1.output) -- ++(0.6,0) |- (andR.input 1);

    % D directly to lower AND (S)
    \draw (D) -- ++(1.3,0) |- (andS.input 1);

    % CLK to both AND gates
    \draw (clkright) |- (andR.input 2);
    \draw (clkdown)  |- (andS.input 2);

    % AND outputs to SR latch
    \draw (andR.output) -- ++(1,0) -- (5.8,0.7);
    \draw (andS.output) -- ++(1,0) -- (5.8,-1.2);

\end{tikzpicture}

\end{document}
```


Again, we analyse the latch by writing the truth table. For convenience the internals nodes $\overline D$, $S$ and $R$. If $\text{CLK} = 0$, then both $S$ and $R$ are false, regardless of $D$. If $\text{CLK} = 1$, one $\text{AND}$ gate will produce $\text{TRUE}$ and the other $\text{FALSE}$, depending on the value of $D$. Given $S$ and $R$, then $Q$ and $\overline Q$ are completely determined. If $\text{CLK} = 0$, then $Q = Q_\text{prev}$ and $\overline Q = \overline{Q_\text{prev}}$. When $\text{CLK}$, $Q =D$. In all cases, $\overline Q$ is the complement of $Q$, as would seem logical. 

This means that when $\text{CLK} = 1$, then latch is *transparent*. the data at $D$ flows through $Q$ as if the latch were just a buffer. When $\text{CLK} = 0$, the latch is *opaque*. If blocks the new data from flowing to $Q$, and $Q$ remembers the old value. Hence, the D latch is sometimes called a *transparent latch* or *level-sensitive latch*. 

## D Flip Flop
A *D flip-flop* can be built from back-to-back D latches controlled by complementary clocks. The first latch $\text{L1}$, is called the *master*. The second latch, $\text{L2}$, is called the *slave*. The node between them is named $\text{N1}$.
![[Pasted image 20251214200137.png]]
A symbol for the D flip-flop is given by $(b)$, and if we don't need $\overline Q$, we can condense it to $(c)$. 

When $\text{CLK} = 0$, the master latch is transparent and the slave is opaque. Therefore, whatever value was at $D$ propagates through to $\text{N1}$. When $\text{CLK} = 1$, the master foes opaque and the slave becomes transparent. The value at $\text{N1}$ propagates to $Q$, but $\text{N1}$ is cut off from $D$. Hence, whatever value was at $D$ immediately before the clock rises from $0$ to $1$ gets copies to $Q$ immediately after the clock rises. At at all other times, $Q$ retains its old value, because there is always an opaque latch blocking the path between $D$ and $Q$. 

This means that a *D flip-flop copies $D$ to $Q$ on the rising edge of the clock, and remembers its state at all other times.* A D flip-flop is also known as a *master-slave flip-flop*, and *edge-triggered flip-flop*, or a *positive edge-triggered flip-flop*. The triangle in the symbols denotes an edge-triggered clock input. The $\overline Q$ output is often omitted when it is not needed. 

### Register

An $N$-bit is a bank of $N$ flip-flops that share a common $\text{CLK}$ input, so that all bit of the register are updated at the same time. Registers are the key building block of most sequential circuits. 

## Enabled Flip-Flops
An *enabled flip-flop* adds another input called $\text{EN}$ or $\text{ENABLE}$ to determine whether data is loaded on the clock edge. When $\text{EN}$ is $\text{TRUE}$, the enabled flip-flop behaves an ordinary D flip-flop. When $\text{EN}$ is $\text{FALSE}$, the enabled flip-flop ignores the clock and retains its state. Enabled flip-flops are useful when we wish to load a new value into a flip-flop only some of the time, rather than every clock edge. 

The most common way to maye an enabled flip-flop is to add a multiplexer. The input multiplexer chooses whether to pass the value at $D$, if $\text{EN}$ is $\text{TRUE}$, or to recycle the old state from $Q$, if $\text{EN}$ is $\text{FALSE}$. Another way do this is to have a *gated clock*. If $\text{EN}$ is $\text{TRUE}$, the $\text{CLK}$ input to the flip-flop toggles normally. If $\text{EN}$ is $\text{FALSE}$, the $\text{CLK}$ inputs is $\text{FALSE}$ and the flip-flop retains its old value. 
![[Pasted image 20251214203014.png]]

Notice that $\text{EN}$ must not change while $\text{CLK} =1$, lest the flip-flop see a clock *glitch* (switch at an incorrect time). Generally, performing logic on the clock is a bad idea.

## Reset-able Flip-Flop
A *reset-able flip-flop* adds another inputs called $\text{RESET}$. When $\text{RESET}$ is $\text{FALSE}$, the reset-able flip-flop behaves like an ordinary D flip-flop. When $\text{RESET}$ is $\text{TRUE}$, the reset-able flip-flop ignores $D$ and resets the output to $0$. Reset-able flip-flop are useful when we want to force a known state into all flip-flops in a system when we first turn it on.

