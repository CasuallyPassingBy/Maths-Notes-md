---
tags:
  - NeuralNetworks
---
Subjects: [[Neural Networks]]
Links: [[Gradient Descent for FFNN]]

Let's begin with a notation which lets us refer to weights in the network in an unambiguous way. We'll use $w^l_{jk}$ to denote the weight for the connection from the $k$th neuron in the $(l-1)$th layer to the $j$th neuron in the $l$th layer. Similarly, for the networks biases and activations. Explicitly, we use $b_j^l$ for the bias of the $j$th neuron in the $l$th layer, and $a^l_j$ for the activation of the $j$th neuron in the $l$th layer. 

With these notations, the activation $a^l_j$ of the $j$th neuron in the $l$th layer is related to the activations in the $(l-1)$th layer by que equation: $$a^l_j = \sigma\left(\sum_k w_{jk}^l a_k^{l-1} + b_j^l\right),$$where the sum is over all neurons $k$ in the $(l-1)$th layer. We want to rewrite this expression in a matrix form we define a *weight matrix* $w^l$ for each layer $l$. The entries of the weight layer $w^l$ are just the weights connecting to the $l$th layer of neurons, the entry $j$th row and $k$th column is $w^l_{jk}$. Similarly, for each layer $l$ we define a *bias vector*, $b^l$. 

With these notations in mind, we can write the equation above in the beautiful and compact vectorised form $$a^l = \sigma(w^l a^{l-1}+ b^l).$$
We would like to consider the intermediate quantity $z^l := w^l a^{l-1} +b^l$, called the *weighted input* to the neurons in layer $l$. 

# Assumptions about the Loss function

Our goal of backpropagation is to compute the partial derivatives $\partial L/\partial w$ and $\partial L/\partial b$ of the loss function $L$ with respect to any weight $w$ or bias $b$ in the network. For backpropagation to work we need to make two main assumptions about the loss function. 
- We need is that the cost function can be written as an average $L = \frac1n\sum_x L_x$ for loss functions $L_x$ for individual training examples, $x$. 
- The loss function is that it can be written as a function of the outputs from the neural network. 

The reason we need the first assumption is because what backpropagation actually lets us fo is compute the partial derivatives $\partial L_x/\partial w$ and $\partial C_x/\partial b$ for a single training example. We then recover $\partial L/\partial w$ and $\partial L/\partial b$ by averaging over training examples. 

# The Fundamental Equations

Backpropagation is about understanding how changing the weights and biases in a network changes the loss function. Ultimately, this means computing the partial derivatives $\partial L/\partial w_{jk}^l$ and $\partial L/\partial b_{j}^l$. But to compute those, we first introduce an intermediate quantity, $\delta_j^l$, which we call the *error* in the $j$ neuron in the $l$th layer. 

We define the error $\delta^l_j$ of the $j$the neuron in the layer $l$ by $$\delta^l_j := \frac{\partial L}{\partial z_j^l}.$$As per usual, we use $\delta^l$ to denote the vector of errors associated with layer $l$. 

The four fundamental equations are
$$\begin{align*}
\delta^L &= \nabla_a L \odot \sigma'(z^L)\\
\delta^l &= ((w^{l+1}) \delta^{l+1})\odot \sigma'(z^l) \\
\dfrac{\partial L}{\partial b^l_j} &= \delta^l_j \\
\dfrac{\partial L}{\partial w_{jk}^l} &= a_k^{l-1} \delta^l_j
\end{align*}$$Where we are considering $\odot$ as the Hadamard product. 

# Backpropagation Algorithm

We are considering a neural network with loss function $L$ and activation function $f$. 

- **Input $x$:** Set the correspondinf activation $a^1$ for the input layer.
- **Feedforward:** for each layer $l = 2, \dots, L$, we compute $z^l = w^l a^{l-1}+b^l$ and $a^l = \sigma(z^l).$
- **Output error $\delta^L$:** Compute the vector $\delta^L = \nabla_a L \odot f'(z^L)$. 
- **Backpropagete the error:** For each $1<l < L$ compute $\delta^l = ((w^{l+1}) \delta^{l+1})\odot f'(z^l)$.
- **Output:** The gradient of the cost function is given by $$\begin{align*}\dfrac{\partial L}{\partial b^l_j} &= \delta^l_j \\
\dfrac{\partial L}{\partial w_{jk}^l} &= a_k^{l-1} \delta^l_j.\end{align*}$$
We want to combine this algorithm with stochastic gradient descent. In particular, given a mini-batch of $m$ training examples, the following algorithm applies a gradient descent learning step based on that mini batch:

- **Input a set of training examples.**
- **For each training example $x$** Set the corresponding input activation $a^{x, 1}$ and perform the following steps:
	- **Feedforward:** For each $l =2,\dots, L$ compute $z^{x, l} = w^l a^{x, l-1}+b^l$ and $a^{x, l} = \sigma(z^{x, l})$. 
	- **Output error $\delta^{x, L}$:** Compute the vector Compute the vector $\delta^{x,L} = \nabla_a L_x\odot f'(z^L)$. 
	- **Backpropagete the error:** For each $1<l < L$ compute $\delta^{x,l} = ((w^{l+1}) \delta^{x,l+1})\odot f'(z^{x,l})$
- **Gradient descent:** For each $L, L-1,\dots, 2$, update the weights according to the rule $$w^l \mapsto w^l - \frac\eta m\sum_x\delta^{x,l}(a^{x,l-1})^\top$$and the biases according to the rule $$b^l \mapsto b^l - \frac\eta m\sum_x\delta^{x,l}.$$
We have an implementation of that here
```python
def backprop(self, x, y):
	
	"""Return a tuple ``(nabla_b, nabla_w)`` representing the
	gradient for the cost function C_x. ``nabla_b`` and
	``nabla_w`` are layer-by-layer lists of numpy arrays, similar
	to ``self.biases`` and ``self.weights``."""
	
	nabla_b = [np.zeros(b.shape) for b in self.biases]
	nabla_w = [np.zeros(w.shape) for w in self.weights]
	
	# feedforward
	activation = x
	activations = [x] # list to store all the activations, layer by layer
	zs = [] # list to store all the z vectors, layer by layer
	for b, w in zip(self.biases, self.weights):
		z = np.dot(w, activation)+b
		zs.append(z)
		activation = sigmoid(z)
		activations.append(activation)
	
	# backward pass
	
	delta = self.cost_derivative(activations[-1], y) * \
	sigmoid_prime(zs[-1])
	nabla_b[-1] = delta
	nabla_w[-1] = np.dot(delta, activations[-2].transpose())
	
	for l in range(2, self.num_layers):
		z = zs[-l]
		sp = sigmoid_prime(z)
		delta = np.dot(self.weights[-l+1].transpose(), delta) * sp
		nabla_b[-l] = delta
		nabla_w[-l] = np.dot(delta, activations[-l-1].transpose())
	
	return (nabla_b, nabla_w)
```


While the derivation of backpropagation is easiest to understand on a per-example basis, in practice training is done on mini-batches, allowing for a clean vectorized implementation.

```python
def backprop(self, X, Y):
        nabla_b = [np.zeros_like(b) for b in self.biases]
        nabla_w = [np.zeros_like(w) for w in self.weights]
        A, Zs = [X], []
        for b, w in zip(self.biases, self.weights):
            Z = w @ A[-1] + b; A.append(sigmoid(Z)); Zs.append(Z)
        delta = (A[-1] - Y) * sigmoid_prime(Zs[-1])
        nabla_b[-1], nabla_w[-1] = np.sum(delta, axis=1, keepdims=True), delta @ A[-2].T
        for l in range(2, self.num_layers):
            delta = (self.weights[-l+1].T @ delta) * sigmoid_prime(Zs[-l])
            nabla_b[-l] = np.sum(delta, axis=1, keepdims=True)
            nabla_w[-l] = delta @ A[-l-1].T
        return nabla_b, nabla_w
```

This actually gives a boost in performance. 
