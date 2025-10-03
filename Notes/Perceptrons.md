---
tags:
  - NeuralNetworks
---
Subjects: [[Neural Networks]]

We need to define a type of artificial neuron called a *perceptron*. Perceptrons were developed in the 1950s and 1960s by the scientist F. Rosenblatt, inspired by earlier work by W. McCulloh and W. Pitts. Today, its more common to use other models of artificial neurons, in much modern work on neural networds, the main neuron model is one called the *sigmoid neuron*. (This might be a tad outdated, since as far as I know the most common one in modern research is ReLU neurons)

A perceptron takes several binary inputs, $x_1, x_2, \dots,$ and produces a single binary output: 
```tikz
\usepackage{tikz}

\begin{document}
\begin{tikzpicture}[->, >=stealth, node distance=1cm, thick]

% Input labels and arrows
\node (x1) at (-2,1) {$x_{1}$};
\node (x2) at (-2,0) {$x_{2}$};
\node (x3) at (-2,-1) {$x_{3}$};

% Circle (neuron)
\node[circle, draw, minimum size=1cm] (neuron) at (0,0) {};

% Connect inputs to neuron
\draw (x1) -- (neuron);
\draw (x2) -- (neuron);
\draw (x3) -- (neuron);

% Output arrow
\node (out) at (2,0) {output};
\draw (neuron) -- (out);

\end{tikzpicture}
\end{document}
```
Rosenblatt proposed a simple rule to compute the output. He introduced *weights*, $w_1, w_2,\dots,$ real numbers expressing the importance of the respective inputs to the output. The nueron's output $0$ or $1$, is determined by whether the weighted sum $\sum_j w_j x_j$ is less or greated than some *threshold value*. Just like the weights, the threshold is a real number which is a parameter of the neuron. $$\begin{cases}0 &  \sum_j w_j x_j \le \text{threshold}, \\ 1 & \sum_j w_j x_j > \text{threshold}.\end{cases}$$

The perceptron isn't a complete model of human decision-making, and it should seem plausible that a complex network of perceptrons could make quite subtle decisions:
```tikz
\usepackage{tikz}
\usetikzlibrary{positioning}

\begin{document}
\begin{tikzpicture}[->, >=stealth, thick, node distance=1cm]

% Style for neurons
\tikzset{neuron/.style={circle, draw, minimum size=1cm}}

% Input nodes
\node (I1) at (0,2) {};
\node (I2) at (0,1) {};
\node (I3) at (0,0) {};
\node (I4) at (0,-1) {};
\node (I5) at (0,-2) {};
\node[left=0.2cm of I3] {inputs};

% Hidden layer 1
\node[neuron] (H11) at (3,1.5) {};
\node[neuron] (H12) at (3, 0.0) {};
\node[neuron] (H13) at (3,-1.5) {};

% Hidden layer 2
\node[neuron] (H21) at (6,2.25) {};
\node[neuron] (H22) at (6,0.75) {};
\node[neuron] (H23) at (6,-0.75) {};
\node[neuron] (H24) at (6,-2.25) {};
% Output node
\node[neuron] (O) at (9,0) {};
\node[right=0.2cm of O] {output};

% Connect input to hidden layer 1
\foreach \i in {1,2,3,4,5}
  \foreach \j in {1,2,3}
    \draw (I\i) -- (H1\j);

% Connect hidden layer 1 to hidden layer 2
\foreach \i in {1,2,3}
  \foreach \j in {1,2,3,4}
    \draw (H1\i) -- (H2\j);

% Connect hidden layer 2 to output
\foreach \i in {1,2,3,4}
    \draw (H2\i) -- (O);

\end{tikzpicture}
\end{document}

```
In this network, the first column of perceptrons, called the *first layer* of perceptrons, is making $3$ simple decisions, by weighing the input evidence. The percetrons on the second layer are making decisions by weighing up the results in the first layer. We can interpret that the second layer is making more abstract decision than only the first layer. Even more complex decisions can be made by the percetron in the third layer. 

We can simplify the way we describe perceptrons. The condition $\sum_j w_i x_j > \text{threshold}$ is cumbersome, and we can make two notational changes to simplify it. The first is to consider using the dot product so $w\cdot x = \sum_j w_j x_j$, where $w$ and $x$ are vectors whose components are the weights and inputs. The second change is to move the threshold to the other side of the inequality, and replace it what's known as the preceptron's *bias* $b:= -\text{threshold}$. Then we get that $$\begin{cases} 0 & w\cdot x  + b \le 0 \\1 & w\cdot x + b >0\end{cases}$$
We can think of the bias of how easy it get the perceptron to output $1$. 

Another way perceptrons can be used is to compute the elementary logical functions we usually think of as underlying computations, functions such as $\sf AND$, $\sf OR$ and $\sf NAND$. For example we have a perceptron with two inputs, each with weight $-2$, and an overall bias $3.$ 
```tikz
\usepackage{tikz}

\begin{document}
\begin{tikzpicture}[->, >=stealth, node distance=1cm, thick]

% Input labels and arrows
\node (x1) at (-2,1) {$x_{1}$};
\node (x2) at (-2,-1) {$x_{2}$};

% Circle (neuron)
\node[circle, draw, minimum size=1cm] (neuron) at (0,0) {$3$};

% Connect inputs to neuron
% Connect inputs to neuron with weights
\draw (x1) -- node[midway, above] {$-2$} (neuron);
\draw (x2) -- node[midway, below] {$-2$} (neuron);

% Output arrow
\node (out) at (2,0) {output};
\draw (neuron) -- (out);

\end{tikzpicture}
\end{document}
```
We see that $00$, $01$ and $10$ produce an output of $1$, but the input $11$ produces an output of $0$. Thus our preceptron implements a $\sf NAND$ gate. 

We see that, in fact, we can use networks of perceptrons to compute *any* logical function at all. The reason is that the $\sf NAND$ gate is [[Logic Gates|universal]] for computation, that is, we can build any computation up out of $\sf NAND$ gates. It follows that perceptrons are also universal for computation. 

This means that networks of perceptrons can be as poweful as any other computing device. 