---
tags:
  - NeuralNetworks
---
Subjects: [[Neural Networks]]
Links: [[Sigmoid Neurons]], [[Perceptrons]]

Suppose we have the network:
```tikz
\usepackage{tikz}
\usetikzlibrary{positioning}

\begin{document}
\begin{tikzpicture}[->, >=stealth, thick, node distance=1cm]

% Style for neurons
\tikzset{neuron/.style={circle, draw, minimum size=1cm}}
% Hidden layer 1
\node[neuron] (H11) at (3,2.25) {};
\node[neuron] (H12) at (3, 0.0) {};
\node[neuron] (H13) at (3,-2.25) {};

% Hidden layer 2
\node[neuron] (H21) at (6,2.25) {};
\node[neuron] (H22) at (6,0.75) {};
\node[neuron] (H23) at (6,-0.75) {};
\node[neuron] (H24) at (6,-2.25) {};
% Output node
\node[neuron] (O) at (9,0) {};
\node(out) at (12, 0){output};

% Connect hidden layer 1 to hidden layer 2
\foreach \i in {1,2,3}
  \foreach \j in {1,2,3,4}
    \draw (H1\i) -- (H2\j);

% Connect hidden layer 2 to output
\foreach \i in {1,2,3,4}
    \draw (H2\i) -- (O);

\draw (O) -- (out);
\end{tikzpicture}
\end{document}
```
As mentioned earlier, the left most layer in this network is called the *input layer*, and the neurons within that layer are called *input neurons*. The rightmost or *output layer* contains the *output neurons*. The middle layer is called a *hidden layer*, since the neurons in this layer are neither inputs nor outputs.
```tikz
\usepackage{tikz}
\usetikzlibrary{positioning}

\begin{document}
\begin{tikzpicture}[->, >=stealth, thick, node distance=1cm]

% Style for neurons
\tikzset{neuron/.style={circle, draw, minimum size=1cm}}

% Input nodes
\node[neuron] (I1) at (0,3.75) {};
\node[neuron] (I2) at (0,2.25) {};
\node[neuron] (I3) at (0,0.75) {};
\node[neuron] (I4) at (0,-0.75) {};
\node[neuron] (I5) at (0,-2.25) {};
\node[neuron] (I6) at (0,-3.75) {};
\node[left=0.2cm of I3] {inputs};

% Hidden layer 1
\node[neuron] (H11) at (3,2.25) {};
\node[neuron] (H12) at (3, 0.75) {};
\node[neuron] (H13) at (3,-0.75) {};
\node[neuron] (H14) at (3,-2.25) {};

% Hidden layer 2
\node[neuron] (H21) at (6,2.25) {};
\node[neuron] (H22) at (6,0.0) {};
\node[neuron] (H23) at (6,-2.25) {};
% Output node
\node[neuron] (O) at (9,0) {};
\node[right=0.2cm of O] {output};

% Connect input to hidden layer 1
\foreach \i in {1,2,3,4,5,6}
  \foreach \j in {1,2,3, 4}
    \draw (I\i) -- (H1\j);

% Connect hidden layer 1 to hidden layer 2
\foreach \i in {1,2,3,4}
  \foreach \j in {1,2,3}
    \draw (H1\i) -- (H2\j);

% Connect hidden layer 2 to output
\foreach \i in {1,2,3}
    \draw (H2\i) -- (O);

\end{tikzpicture}
\end{document}

```

Somewhat confisingly, such multiple layer networks are sometiles called *multilayer perceptrons* or *MLPs*, despite being made up of sigmoid neurons and not perceptrons. 

The design of the input and output layers in a network is often straightforward, and often dictated by the problem at hand. 

We have been discussing neural networds where the output from one layer is used as input to the next layer. Such networks are called *feedforward neural networks*. This means there are no loops in the network. If we did have loops, we'd end up with sitatuations where the input to the $\sigma$ function depended on the output. 

There are other models of artificial neural networks in which feedback loops are possible. These models are called [[recurrent neural networks]]. The idea in these models is to have neurons which fire for some limited duration of time, before becoming quiescent. That firing can stimulate other neurons, which may fire a little while later, also for a limited duration. 