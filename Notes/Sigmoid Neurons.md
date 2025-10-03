---
tags:
  - NeuralNetworks
---
Subjects: [[Neural Networks]]
Links: [[Perceptrons]]

Supopse we have a network of perceptrons that we'd like to use to learn to solve a problem. We'd like the network to learn the weights and biases so that the output from the network correctly classifies solves the problem. Suppose we make a small change in some weight or bias in the network, what we'd like to is for this small change in weight to cause only a small corresponding change in the output from the network. This property will make learning possible. 
```tikz
\usepackage{tikz}
\usetikzlibrary{positioning}

\begin{document}
\begin{tikzpicture}[->, >=stealth, thick, node distance=1cm]

% Style for neurons
\tikzset{neuron/.style={circle, draw, minimum size=1cm}}

% Input nodes


% Hidden layer 1
\node[neuron] (H11) at (3,1.5) {};
\node[neuron] (H12) at (3, 0.0) {};
\node[neuron] (H13) at (3,-1.5) {};

% Hidden layer 2
\node[neuron] (H21) at (6,1.5) {};
\node[neuron] (H22) at (6,0.0) {};
\node[neuron] (H23) at (6,-1.5) {};

% Output node
\node[neuron] (O) at (9,0) {};
\node(out) at (12, 0){output + $\delta$output};


\draw (H11)  -- node[midway, above] {$w+ \Delta w$} (H21);

% Connect hidden layer 1 to hidden layer 2
\foreach \i in {1,2,3}
  \foreach \j in {1,2,3}
    \draw (H1\i) -- (H2\j);

% Connect hidden layer 2 to output
\foreach \i in {1,2,3}
    \draw (H2\i) -- (O);

\draw (O) --(out);
\end{tikzpicture}
\end{document}
```

If it were true that a small change in a weight or bias causes only a small change in output, then we could use this fact to modify the weights and biases to get out network to behave in the manner we want. We could nudge the weights and biases such that it gets closed to the desired behaviour. 

We can overcome this problem by introducing a new type of artificial neuron called a *sigmoid* neuron. Sigmoid neurons are similar to perceptrons but modified so that small changes in their weights and biases cause only a small change in their output. 

We'll depict sigmoid neurons in the same way we depicted perceptrons: 
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
Just like a preceptron, the sigmoind neurons has inputs, $x_1, x_2,\dots,$ but instead of being $0$ or $1$, these inputs take values on $[0, 1]$. Just like perceptrons, the sigmoid neurons have weights and biases for each input $w_1,\dots$, and an over all bias $b$. The output is $\sigma(w\cdot x +b)$, where $$\sigma(x) := \frac1{1+ e^{-x}}.$$To put it more explicitly, we get that the output of a sigmoid neuron with inputs $x_1, x_2,\dots,$ weights $w_1, w_2, \dots,$ and bias $b$ is $$\frac1{1+\exp(-\sum_j w_j x_j - b)}$$Let $z := w\cdot x + b$. If $z\gg 0$, then $\sigma(z) \approx 1$. On the other hand if $z \ll 0$, then $\sigma(z) \approx 0$. This means that the behaviour of a sigmoid neuron also closely approximates a perceptron. 

By using $\sigma$ we get a smooth perceptron. This smoothness of $\sigma$ is crucial. The smoothness of $\sigma$ means that small changes $\Delta w_j$ in the weights and $\Delta b$ in the bias will produce a small change $\Delta\text{output}$ in the output from the neuron. We know that $$\Delta\text{output} \approx \sum_{j} \frac{\partial \text{output}}{\partial w_j}\Delta w_j + \frac{\partial \text{output}}{\partial b}\Delta b.$$
Later we will consider neurons where the output is $f(w\cdot x  + b)$ for some other *activation fucntion* $f(\cdot)$. The main thing that changes when we use a different activation function is that the particular values for the partial derivatives change. 