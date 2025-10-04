---
tags:
  - NeuralNetworks
---
Subjects: [[Neural Networks]]
Links: [[Gradient Descent for FFNN]], [[Feedforward Neural Networks]]


```python
import micropip
await micropip.install("numpy")
```
This is just to have numpy be available. 

```python
import random, numpy as np

class Network:
    def __init__(self, sizes):
        self.sizes, self.num_layers = sizes, len(sizes)
        self.biases = [np.random.randn(y, 1) for y in sizes[1:]]
        self.weights = [np.random.randn(y, x) for x, y in zip(sizes[:-1], sizes[1:])]

    def feedforward(self, a):
        for b, w in zip(self.biases, self.weights):
            a = sigmoid(w @ a + b)
        return a

    def SGD(self, training_data, epochs, batch_size, eta, test_data=None):
        n = len(training_data)
        for j in range(1, epochs+1):
            random.shuffle(training_data)
            for k in range(0, n, batch_size):
                self.update(training_data[k:k+batch_size], eta)
            if test_data:
                print(f"Epoch {j}: {self.evaluate(test_data)} / {len(test_data)}")

    def update(self, mini_batch, eta):
        X = np.hstack([x for x, _ in mini_batch])
        Y = np.hstack([y for _, y in mini_batch])
        nabla_b, nabla_w = self.backprop(X, Y)
        m = len(mini_batch)
        self.weights = [w - (eta/m) * dw for w, dw in zip(self.weights, nabla_w)]
        self.biases  = [b - (eta/m) * db for b, db in zip(self.biases, nabla_b)]

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

    def evaluate(self, test_data):
        return sum(int(np.argmax(self.feedforward(x)) == y) for x, y in test_data)

def sigmoid(z): return 1/(1+np.exp(-z))
def sigmoid_prime(z): return sigmoid(z)*(1-sigmoid(z))

```

This gives us a full neural network with MSE as its loss function, and sigmoid as the activation function. 