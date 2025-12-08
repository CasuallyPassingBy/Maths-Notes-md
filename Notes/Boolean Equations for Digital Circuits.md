---
tags:
  - DigitalCircuits
---
Subjects: [[Digital Circuits]]
Links: [[Logic Gates]], [[Boolean Algebra]]

The *complement* if a variable $A$ is its inverse $\overline A$. The variable complement is called a *literal*. We call $A$ the *true form* of the variable and $\overline A$ the *complementary form*. 

The $\text{AND}$ of one one or more literals is called a *product* or an *implicant*. A *minterm* is a product involving all of the inputs to the function. Similarly, the $\text{OR}$ of one or more literals is called a *sum*. A *maxterm* is a sum involving all the inputs to the function. 

The *order of operations* is important when interpreting Boolean operations. In Boolean equations, $\text{NOT}$ has the highest precedence, followed by $\text{AND}$, then $\text{OR}$. 

## Sum-of-Products Form
A truth table of $N$ inputs contains $2^ N$ rows, one for each possible value of the inputs. Each row in a truth table is associated with a minterm that is $\text{TRUE}$ for that row. The minterms are numbered with $0$; the top row corresponds to minterm $0$, $m_0$, the next row to minterm $1$, $m_1$, and so on. 

We can write a Boolean equation for any truth table by summing each of the minterms for which the output, $Y$, is $\text{TRUE}$. 

This called the *sum-of-products canonical form* of a function because it is the sum of products. Although there are many ways to write the same function, we will sort the minterms in the same order as they appear in the truth table. The sum-of-prodcut canonical form can also be written in *sigma notation* using the summation symbol, $\Sigma$. With this notation, a function can be written as $$\Sigma(m_{i_1},\dots, m_{i_k}) = \Sigma(i_1, \dots, i_k) $$where $m_{i_1},\dots m_{i_k}$ are $\text{TRUE}$ minterms.

## Product-of-Sums Form
An alternative way of expressing Boolean functions is the *product-of-sums canonical form* Each row of a truth table corresponds to a maxterm that is $\text{FALSE}$ for that row. We can write a Boolean equation for any circuit directly from the truth table as the $\text{AND}$ of each the maxterms for which the outputs is $\text{FALSE}$. The product-of-sums canonical form can also be written in *pi notation* using the product, symbol $\Pi$.

# From Logic to Gates

A *schematic* is a diagram of a digiral circuit showing the elements and the wires that connect them together. By drawing schematics in a consistent fashion, we make them easier to read and debug. We will generally obey the following guidelines:
- Inputs are on the left (or top) of an schematic.
- Outputs are on the right (or bottom) side of a schematic.
- Whenever possible, gates should flow from the left to right.
- Straight wires are better to use than wires with multiple corners. 
- Wire always connect at a $T$ junction.
- A dot where wires cross indicate a connection between the wires.
- Wires crossing *without* a dot make no connection. 

Any Boolean equation in sum-of-products form can be drawn as a schematic in a systematic way. First, draw columns for the inputs. Place inverters in adjacent columns to provide the complementary inputs if necessary, Draw rows of $\text{AND}$ gates for each of the minterms. Then, for each output draw an $\text{OR} gate connected to the minters leated to that output. 

This style is called a *programmable logic array (PLA)* becayse the inverters, $\text{AND}$ gates, and $\text{OR}$ gates are arrayed in a systematic fashion. 

# Multilevel Combinational Logic

Logic in sum-of-product form is called a *two-level logic* because it consists of literals connected to a level of $\text{AND}$ gates connected to a level of $\text{OR}$ gates. Designer often build circuits with more than two levels of logic gates. These multileveled combinational circuits may use less hardware than their two-level counterparts. 

## Hardware Reduction
Some logic functions requiere an enormous amount of hardware when built using a two-level logic. $N$-input $\text{XOR}$ produces $\text{TRUE}$ output when an odd number of inputs are $\text{TRUE}$. We can write logic formula as its sum-of-products form, but we would need as many as $2^{N-1}$ $\text{AND}$ gates. We can use the fact that $\text{XOR}$ is an associative operation, and concatenate two input $\text{XOR}$ gates.

Selecting the best multileveled implementation of a specific logic function is not a simple process. Moreover 'best' has many meanings: fewest gates, fastest, shortest design time, least cost, least power consumption. In CMOS, $\text{NAND}$s and $\text{NOR}$s are more efficient, which also changes how we consider best.

## Bubble Pushing
As we know CMOS circuits prefer $\text{NAND}$s and $\text{NOR}$s over $\text{AND}$s and $\text{OR}$s. Reading the equation by inspection from a multilevel circuit with $\text{NAND}$s and $\text{NOR}$s can be pretty complicated. Bubble pushing is a helpful way to redraw there circuits so that the bubbles cancel out and the function can be more easily determined. 
- Begin at the output of the circuits and work toward the input.
- Push any bubbles on the final output back towards the inputs so that you can read an equation in  terms of the output.
- Working backward, draw each gate in the form so that bubbles cancel. If the current gate has an input bublle, draw the preceding gate with an output bubble. If the current gate doesn't have an input bubble, draw the preceding gate without an output bubble.

# $X$'s and $Z$'s
Boolesn algebra is limited to $0$'s and $1$'s. However, real circuits can also have illegal and floating values, represented symbolically by $X$ and $Z$.

The symbol $X$ indicates that the circuit mode has an *unknown* or *illegal* value. This commonly happens if it is being driven to both $0$ and $1$ at the same time. This situation, called *contention*, is considered to be an error and must be avoided. The actual voltage on a note with contention may be somewhere between $0$ and $V_{DD}$, depending on the relative strength of the gates driving $\text{HIGH}$ and $\text{LOW}$. It is often in the forbidden zone. Contention can cause large amounts of power to flow between the fighting gates, resulting in the circuit getting hot and possibly damaged.

When $X$ appears in truth tables, it indicates that the value of the variable is unimportant.

The symbol $Z$ indicates that a node is being driven neither $\text{HIGH}$ nor $\text{LOW}$. The node is said to be *floating, high impedance,* or *high $Z$*. A floating node might be $0$, might be $1$, or might be ar some voltage between, depending on the history of the system. A floating voltage does not always mean there is an error in the circuit,

One common way to produce a floating node is to forget to connect a voltage to a circuit input, or to assume that an unconnected inputs i s the same as an input with the value of $0.$ This type of mistake will make that the circuits will behave erratically, since even touching it can change how it behaves.

The *tristate buffer* has three possible output states: $1, 0$, and $Z$. The tristate buffer an input $A$, output $Y$, and *enable* $E$. When the enable is $\text{TRUE}$, the tristate buffer acts as a simple buffer, transferring the input value to the output. When the enable is $\text{FALSE}$, the output is allowed to float ($Z$).

```tikz
\usepackage{tikz}
\usetikzlibrary{positioning, circuits.logic.US}

\makeatletter%
%
%
\pgfdeclareshape{tri state buffer active high}{
    \inheritsavedanchors[from=buffer gate US]
    \inheritanchorborder[from=buffer gate US]
    \inheritanchor[from=buffer gate US]{center}
    \inheritanchor[from=buffer gate US]{base}
    \inheritanchor[from=buffer gate US]{base west}
    \inheritanchor[from=buffer gate US]{base east}
    \inheritanchor[from=buffer gate US]{mid}
    \inheritanchor[from=buffer gate US]{mid west}
    \inheritanchor[from=buffer gate US]{mid east}
    \inheritanchor[from=buffer gate US]{north}
    \inheritanchor[from=buffer gate US]{north west}
    \inheritanchor[from=buffer gate US]{north east} 
    \inheritanchor[from=buffer gate US]{south}
    \inheritanchor[from=buffer gate US]{south east}
    \inheritanchor[from=buffer gate US]{south west}
    \inheritanchor[from=buffer gate US]{west}
    \inheritanchor[from=buffer gate US]{east}
    \inheritanchor[from=buffer gate US]{input}
    \inheritanchor[from=buffer gate US]{output}
    \anchor{control}{%
        \dimensions
        \pgfpointintersectionoflines{\csname pgf@anchor@buffer gate US@north west\endcsname}{\tipanchor}{\centerpoint}{\centerpoint\advance\pgf@y1pt}%
    }%
    \backgroundpath{%
        \dimensions%
        \pgf@xc\halfwidth%
        \pgf@yc\halfheight%
        \advance\pgf@xc-\outerxsep%
        \advance\pgf@yc-\outerysep%
        {%
            \pgftransformshift{\centerpoint}%
            \pgfpathmoveto{\tipanchor}%
            \pgfpathlineto{\pgfqpoint{-.833333\pgf@xc}{1.166666\pgf@yc}}%
            \pgfpathlineto{\pgfqpoint{-.833333\pgf@xc}{-1.166666\pgf@yc}}%
            \pgfpathclose%
            %
            % Draw the input.
            %
            \expandafter\ifx\expandafter\pgf@lib@sh@itext\csname input-1\endcsname%
                {%
                    \pgfpathcircle{%
                        \pgf@xa\halfside%
                        \pgf@x-.833333\pgf@xa%
                        \advance\pgf@x-.5\pgflinewidth%
                        \advance\pgf@x-\invertedradius%
                        \pgf@y0pt%
                    }{+\invertedradius}%                
                }%
            \fi%                
        }%
    }%
}

\pgfdeclareshape{tri state buffer active low}{
    \inheritsavedanchors[from=buffer gate US]
    \inheritanchorborder[from=buffer gate US]
    \inheritanchor[from=buffer gate US]{center}
    \inheritanchor[from=buffer gate US]{base}
    \inheritanchor[from=buffer gate US]{base west}
    \inheritanchor[from=buffer gate US]{base east}
    \inheritanchor[from=buffer gate US]{mid}
    \inheritanchor[from=buffer gate US]{mid west}
    \inheritanchor[from=buffer gate US]{mid east}
    \inheritanchor[from=buffer gate US]{north}
    \inheritanchor[from=buffer gate US]{north west}
    \inheritanchor[from=buffer gate US]{north east} 
    \inheritanchor[from=buffer gate US]{south}
    \inheritanchor[from=buffer gate US]{south east}
    \inheritanchor[from=buffer gate US]{south west}
    \inheritanchor[from=buffer gate US]{west}
    \inheritanchor[from=buffer gate US]{east}
    \inheritanchor[from=buffer gate US]{input}
    \inheritanchor[from=buffer gate US]{output}
    \anchor{control}{%
        \dimensions
        \tipanchor%
        \pgf@xa\pgf@x%  
        \pgf@ya\pgf@y%
        \csname pgf@anchor@buffer gate US@north west\endcsname%
        \advance\pgf@xa-\pgf@x%
        \advance\pgf@ya-\pgf@y%
        \pgfpointintersectionoflines{\csname pgf@anchor@buffer gate US@north west\endcsname}{\tipanchor}{\centerpoint}{\centerpoint\advance\pgf@y2pt}%
        \pgfmathparse{sqrt(\pgf@xa^2+\pgf@ya^2)/\pgf@xa*\invertedradius}
        \advance\pgf@y\pgfmathresult pt
        \advance\pgf@y\invertedradius
    }%
    \backgroundpath{%
        \dimensions%
        \pgf@xc\halfwidth%
        \pgf@yc\halfheight%
        \advance\pgf@xc-\outerxsep%
        \advance\pgf@yc-\outerysep%
        {%
            \pgftransformshift{\centerpoint}%
            \pgfpathmoveto{\tipanchor}%
            \pgfpathlineto{\pgfqpoint{-.833333\pgf@xc}{1.166666\pgf@yc}}%
            \pgfpathlineto{\pgfqpoint{-.833333\pgf@xc}{-1.166666\pgf@yc}}%
            \pgfpathclose%
            %
            % Draw the input.
            %
            \pgfpathcircle{%
                \tipanchor%
                \pgf@xa\pgf@x%  
                \pgf@ya\pgf@y%
                \csname pgf@anchor@buffer gate US@north west\endcsname%
                \advance\pgf@xa-\pgf@x%
                \advance\pgf@ya-\pgf@y%
                \pgfpointintersectionoflines{\csname pgf@anchor@buffer gate US@north west\endcsname}{\tipanchor}{\centerpoint}{\centerpoint\advance\pgf@y1pt}%
                \pgfmathparse{sqrt(\pgf@xa^2+\pgf@ya^2)/\pgf@xa*\invertedradius}
        \advance\pgf@y\pgfmathresult pt
                }{+\invertedradius}%
            \expandafter\ifx\expandafter\pgf@lib@sh@itext\csname input-1\endcsname%
                {%
                    \pgfpathcircle{%
                        \pgf@xa\halfside%
                        \pgf@x-.833333\pgf@xa%
                        \advance\pgf@x-.5\pgflinewidth%
                        \advance\pgf@x-\invertedradius%
                        \pgf@y0pt%
                    }{+\invertedradius}%                
                }%
            \fi%                
        }%
    }%
}

\tikzset{
    circuit declare symbol=tri state buffer active low,
    set tri state buffer active low graphic={draw, shape=tri state buffer active low, minimum size=5mm},
    circuit declare symbol=tri state buffer active high,
    set tri state buffer active high graphic={draw,shape=tri state buffer active high,minimum size=5mm}
}

\begin{document}

%
\begin{tikzpicture}[circuit logic US, on grid]
\node (i) {A};
\node (buf) [right of=i, tri state buffer active high] {};
\node (ctrl) [above=of buf] {E};
\node (o) [right of=buf] {Y};

\draw (i) -- (buf.input)
    (ctrl) -- (buf.control)
    (buf.output) -- (o);
\end{tikzpicture}%

\begin{tikzpicture}[circuit logic US, on grid]
\node (i) {A};
\node (buf) [right of=i, tri state buffer active low] {};
\node (ctrl) [above=1 of buf] {$\overline E$};
\node (o) [right of=buf] {Y};

\draw (i) -- (buf.input)
    (ctrl) -- (buf.control)
    (buf.output) -- (o);
\end{tikzpicture}%
\end{document}
```

The buffer on the right is called an *active high* enable. That is the enable is $\text{HIGH}%, the buffer is enabled. The buffer on the left is called an *active low buffer*. When the buffer is $\text{LOW}$ the buffer is enabled. We show that the signad is active low by putting a bubble on its input wire. We often indicate an activel low input by drawing a bar over its name, $\overline E$, or appening the letter 'b' or 'bar' after the name $Eb$ or $Ebar$. 
