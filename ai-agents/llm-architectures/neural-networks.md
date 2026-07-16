# But what is a neural network?
As the name suggests neural networks are machine learning models inspired by the human brain. It stacks simple "neurons" in layers and learns pattern-recognizing weights and biases from data to map inputs to outputs.

What distinguishes neural networks from other traditional machine learning algorithms is their layered structure and their ability to perfrom nonlinear transformation.
## What is a neuron?
One can think of neuron as something that holds a number. This number is called "Activation". It can perform computation of a function.
## Weights and Biases
Weights controls how strongly each input feature influences the final output.

Biases are built-in values that shift the decision threshold allowing the neurons to activate even if the input signal themselves are weak or put another way how high the weighted sum needs to be before the neuron starts getting meaningfully active.

Together these ***model parameters*** determine how each neuron contributes to the overall computation.

## Layers

-**Input layer**: receives the raw features.
   
-**Hidden layers**:  The computational heavy layers. Multiple hidden layers perform complex mathematical transformations to extract features and learn hidden patterns.

-**Output layer**: Produces the final result, such as classification or prediction.


Just like other machine learning algorithms, a neural net requires rigorous training to perform well on testing. To train a network, a single neuron computes: 

## Neural Network training
$z =∑wx+b$

$a=σ(z)$

- x: input features
- w: weight
- b: bias
- z: weighted sum
- σ: activation function(transforms the linear combination to fit the decision of the function)
- a: output

The neural net trains in four steps:

1. Forward pass: Inputs flow through the network, computing linear combinations, passing through the nonlinear activation function and producing an output prediction.

2. Error calculation: The loss function measures the difference between prediction and truth.

3. Backward pass (backpropagation): The error is propagated backward through the network. At each neuron, the algorithm calculates how much each weight and bias contributed to the error using the chain rule of calculus.

4. Weight update: The weights and biases are adjusted slightly in the direction that reduces the error, using an optimization method like gradient descent.

This process is repeated many times over the training dataset.