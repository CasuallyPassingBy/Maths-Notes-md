---
tags:
  - NeuralNetworks
---
Subjects: [[Neural Networks]]
Links: [[Feedforward Neural Networks]], [[Sigmoid Neurons]], [[The Gradient]]

What we'd like is an algorith which lets us find weights and biases so that the output from the network approximates $y(x)$ for all training inputs $x$. To quantify how well we're achieving this goal we define a *loss/cost/objective function*: $$L(w, b) := \frac1{2n}\|y(x) -a \|^2.$$Here, $w$ denotes the collection of all weights in the network, $b$ all the biases, $n$ is the total number of training inputs, and $a$ is the vector of outputs from the network when $x$ is input, and the sum is over all training inputs $x$. We call $L$ the *quadratic loss function*; it's also sometimes known as the *mean squared error* or just *MSE*. 

We see that when we minimise $L(w,b )$ becomes small, it is when $y(x)$ is approximately equal to $a$, for all training inputs $x$. So our training algorithm has done a good job if it can find weights and biases so that $L(w, b) \approx 0$. The goal of our training is to minimise the loss function $L(w, b)$ as a function of the weights and biases. In other words, we want to find a set of weights and biases which make the loss as small as possible.

# Gradient Descent

Let's suppose we are trying to minimise the some function $C(v)$. This could be any real-valued function of many variables, $v = v_1,v_2, \dots$. We know that $\Delta C$ can be approximated using $$\Delta C \approx \nabla C \cdot \Delta v.$$Since $\nabla C$ is points at the direction of most growth, we can no consider if we took a step with direction $-\nabla C$. In particular suppose we choose $$\Delta v = -\eta\nabla C,$$where $\eta$ is a small positive parameter, called the *learning rate*. Then we get that $$ \Delta C \approx -\eta \nabla C \cdot \nabla C = -\eta \|\nabla C\|^2.$$This means that $C$ will always decrease, and never increase, if we change $v$ according to the change we defined, This the property we desired. Thus we will use the the equality above to compute the value of $\Delta v$, then move th to the position $v$ by that amount: $$v \mapsto v' = v-\eta \nabla C(v).$$This update rule is defining the gradient descent algorithm. It gives us a way of repeatedly changing the position $v$ in order to find a minimum of the function $C$.

Let's suppose that we're trying to make a move $\Delta v$ in position so as to decrease $C$ as much as possible. This is equivalent to minimising $\Delta C \approx \nabla C \cdot \Delta v$. If we constain the ise of $\|\Delta v\| =\varepsilon$, for some $\varepsilon >0$, then the choise of $\Delta v$ which minimises $\nabla C \cdot \Delta v$ is $\Delta v = -\eta \nabla C$, where $\eta = \varepsilon/\|\nabla C\|$. 

There are several variations of gradient descent, including variations that more closely mimic a real physical ball rolling down hill. These ball-mimicking variations have some advantages, but also have a major disadvantage: it turn out to be necessary to compute second partial derivatives of $C$, and can be quite costly.

## Stochastic Gradient Descent

The idea is to use gradient descent to find the weights $w_k$ and biases $b_l$ which minimise the loss function. Wriring out the gradient descent update rule in terms of components, we have $$\begin{align*}w_k' &= w_k - \eta \frac{\partial C}{\partial w_k} \\ b_l' &= b_l - \eta \frac{\partial C}{\partial b_l}.\end{align*}$$By repeatedly applying this update rule we can minimise the loss function. 

Let's look back on the quadratic loss function. Let us see that has the form $C = \frac1n \sum_x C_x$, meaning that is an average of losses $C_x:= \|y(x)-a\|^2/2$ for individual training examples. By linearity of the gradient we get that $\nabla C = \frac1n\sum_x  \nabla C_x.$ There's a caveat, when the number of training inputs is very large this can take a long time, and learning thus occurs slowly.

An idea called *stochastic gradient descent* can be used to speed up learning. The idea is to estimate $\nabla C$ by computing $\nabla C_x$ for a small sample of randomly chosen training inputs. By averaging over this small sample it turn out that we can quickly get a good estimate of the true gradient $\nabla C$, and this helps us speed up gradient descent and learning. 

Making things a little bit more precises, stochastic gradient descent works by randomly picking out a small number $m$ of randomly chosen training inputs. We'll label those random training inputs $X_1, X_2, \dots, X_m$, and refer to them as a *mini-batch*. Provided the sample $m$ is large enough we expect that the average value of $\nabla C_{X_j}$ will be roughly equal to the average over all $\nabla C_x$, i.e. $$\nabla C \approx \frac1m\sum_{j = 1}^m \nabla C_{X_j}.$$
Connecting this explicitly to learning in neural networks, suppose $w_k$ and $b_l$ denote the weights and the biases in neural networks. Then stochastic gradient descent works by picking out a randomly chosesn mini-batch of training inputs, and training with those $$\begin{align*}w_k' &= w_k - \frac{\eta}{m}\sum_{j = 1}^m\frac{\partial C_{X_j}}{\partial w_k}  \\ b_l' &= b_l - \frac{\eta}{m}\sum_{j = 1}^m\frac{\partial C_{X_j}}{\partial b_l}.\end{align*}$$
Then we pick out another randomly chosen mini-batch and train with those. And so on, until we've exhausted the training inputs, which is said to complete an *epoch* of training. At that point we start over with a new training epoch. 

A special version of stochastic gradient descent is when the mini-batch size is $1$, meaning, that given a training input $x$, we update out weights and biases according to the rules $$\begin{align*}w_k' &= w_k - \eta \frac{\partial C_x}{\partial w_k} \\ b_l' &= b_l - \eta \frac{\partial C_x}{\partial b_l}.\end{align*}$$Then we choose another training input, and update the weights and biases again. This procedure is known as *online*, *on-line*, or *incremental* learning. In online learning, a neural network learns from just one training input at a time. 