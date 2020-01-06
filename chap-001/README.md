# Chapter 001
In this chapter we'll write a computer program implementing a neural network that learns
to recognize handwritten digits.
The program uses no special neural network libraries, but can recognize digits with an
accuracy of over 96 percent.

# Key Topics
* Two important types of artificial neurons
    - The **Perceptron**
    - The *Sigmoid* neuron
* The standard learning algorithm for neural networks, known as *stochastic gradient
    descent*

# Perceptron
Developed in the 1950s and 1960s by the scientist *Frank Rosenblatt* inspired by earlier
work by *Warren McCulloch* and *Walter Pitts*.
Today it's more common to use other models of artificial neurons more so the Sigmoid
neuron.
## How perceptrons work
A perceptron takes several binary inputs, $x_{1},x_{2},...,x_{n}$ and produces a single binary
output:

$y=f(x_{1},x_{2},...,x_{n})$

Rosenblatt proposed a simple rule to compute the output.He introduced weights,
$w_{1},w_{2},...,w_{n}$ ,real numbers expressing the importance of the respective inputs
to the output.
The neuron's output, 0 or 1, is determined by whether the weighted sum $\sum w_{j} x_{j}$ is less than or greater than some *threshold value*.
Just like the weights, the threshold is a real number which is a parameter of the neuron.
More precisely in algebraic terms:

\[
$output =   \Bigg\{ 0 \quad if  \quad \sum \; w_{j}\;x_{j} \quad < \; threshold \quad
\quad
                  1 \quad  if \quad \sum \; w_{j} \; x_{j} \quad > \quad threshold
                  \quad$
\]


We can think of a perceptron as a device that makes decisions by **weighing up evidence**.
We can simplify the equation as a dot product, **w.x**=$\sum \quad w_{j} \; x_{j} \quad$,
where w and x are vectors whose components are the weights and inputs.
The second is to more the threshold to the other side of the inequality, and to replace
what's known as the perceptron's *bias*, $b\; ==\; - threshold$
To have
\[
$output=\{ 0 \; if  \; w.x \; + b <= 0\quad
1 \; if \; w.x \; + b > 0$
\]

 It turns out that we can devise learning algorithms which can automatically tune the weights and biases of a network of artificial neurons. This tuning happens in response to external stimuli, without direct intervention by a programmer. These learning algorithms enable us to use artificial neurons in a way which is radically different to conventional logic gates. Instead of explicitly laying out a circuit of NAND and other gates, our neural networks can simply learn to solve problems, sometimes problems where it would be extremely difficult to directly design a conventional circuit.


## Sigmoid Neurons
Sigmoid neurons are similar to perceptrons, but modified so that small changes in their weights and bias cause only a small change in their output. That's the crucial fact which will allow a network of sigmoid neurons to learn.

Also just like a perceptron, the sigmoid neuron has weights for each input, w1,w2,…, and
an overall bias, b. But the output is not 0 or 1. Instead, it's σ(w⋅x+b), where σ is
called the sigmoid function* *Incidentally, σ is sometimes called the logistic function,
and this new class of neurons called logistic neurons. It's useful to remember this
terminology, since these terms are used by many people working with neural nets. However,
we'll stick with the sigmoid terminology., and is defined by:

\[$ \sigma(z)  = \quad \frac{1}{1 + \exp(-z)}$\]






