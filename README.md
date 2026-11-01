From Biological Neurons to Artificial Neurons

«Understanding how the human brain inspired one of the fundamental building blocks of Artificial Intelligence.»

1. Introduction

The human brain contains billions of neurons that communicate with one another to process information, learn, and respond to external stimuli.

Inspired by this biological network, researchers developed an abstract mathematical model called the Artificial Neuron, which forms the foundation of Artificial Neural Networks (ANNs).

Although biological and artificial neurons operate very differently, they share a fundamental conceptual pattern:

Input → Processing → Output

This note explores how the structure of a biological neuron relates to the mathematical structure of an artificial neuron.

---

2. Understanding a Biological Neuron

A biological neuron is a specialized nerve cell responsible for receiving, processing, and transmitting information through electrical and chemical signals.

Main components

Component| Function
Dendrites| Receive incoming signals from other neurons.
Cell Body (Soma)| Integrates incoming signals and maintains the cell.
Nucleus| Contains genetic material and regulates cellular activities.
Axon| Conducts electrical impulses away from the cell body.
Myelin Sheath| Insulates the axon and increases signal conduction speed.
Axon Terminals| Communicate with other cells, generally through neurotransmitter release.

How does a biological neuron work?

1. Reception: Dendrites receive signals from other neurons.
2. Integration: The cell body integrates incoming signals.
3. Signal generation: If the membrane reaches its firing threshold, an action potential is generated.
4. Transmission: The electrical impulse travels along the axon.
5. Communication: Axon terminals communicate with other neurons or target cells.

This process allows biological neural networks to perform complex information-processing tasks.

---

3. Understanding an Artificial Neuron

An artificial neuron is a mathematical computational unit inspired by biological neurons.

It receives numerical inputs, multiplies them by corresponding weights, adds a bias, and passes the result through an activation function.

Components of an Artificial Neuron

Component| Mathematical representation| Purpose
Inputs| x₁, x₂, ..., xₙ| Features supplied to the neuron
Weights| w₁, w₂, ..., wₙ| Determine the importance of each input
Bias| b| Adjusts the neuron's response
Weighted Sum| z| Combines inputs and weights
Activation Function| f(z)| Introduces a response transformation
Output| y| Result passed to the next computational unit

Step 1: Receive inputs

Consider a neuron receiving three inputs:

- x₁ = 2
- x₂ = 3
- x₃ = 1

Each input represents a numerical feature.

Step 2: Apply weights

Every input has an associated weight.

- w₁ = 0.5
- w₂ = 0.8
- w₃ = 0.2

Weights determine how strongly each input contributes to the result.

Step 3: Add bias and calculate the weighted sum

The neuron calculates:

z = (x₁ × w₁) + (x₂ × w₂) + (x₃ × w₃) + b

Assume b = 0.1.

z = (2 × 0.5) + (3 × 0.8) + (1 × 0.2) + 0.1

z = 0.5 + 2.4 + 0.2 + 0.1

z = 3.2

Step 4: Apply the activation function

The weighted sum is passed through an activation function.

For example, using ReLU:

ReLU(z) = max(0, z)

Therefore:

y = max(0, 3.2)

y = 3.2

The final output is passed to another neuron or used by the model.

---

4. Biological Neuron vs Artificial Neuron

The biological neuron provides inspiration for the artificial neuron, but their implementations are fundamentally different.

Biological system| Artificial neural network
Dendrites receive signals| Inputs receive numerical values
Synaptic connections have varying strengths| Connections have learnable weights
Soma integrates signals| Mathematical summation combines inputs
Neuronal firing threshold| Bias and activation mechanism
Axon transmits impulses| Output is passed to subsequent units
Synaptic plasticity supports learning| Training algorithms update weights and biases

Important: An artificial neuron is a simplified mathematical abstraction. It does not reproduce the full complexity of a biological neuron, including electrochemical signaling, temporal dynamics, and cellular processes.

---

5. What Makes an Artificial Neuron Learn?

An artificial neuron does not automatically know the correct weights.

During model training, the network adjusts its weights and biases to reduce prediction errors.

A simplified learning process:

1. The model receives input data.
2. The neuron calculates an output.
3. The model compares its prediction with the expected result.
4. A loss function measures the prediction error.
5. An optimization algorithm, commonly using gradient descent and backpropagation, updates the parameters.
6. The process repeats over multiple training iterations.

Over time, the network can learn patterns and relationships from data.

---

6. Common Activation Functions

Activation functions help neural networks model nonlinear relationships.

Function| Formula| Common use
ReLU| max(0, z)| Hidden layers
Sigmoid| 1 / (1 + e⁻ᶻ)| Binary classification output
Tanh| (eᶻ - e⁻ᶻ) / (eᶻ + e⁻ᶻ)| Some hidden-layer applications
Linear| f(z) = z| Regression output

Without nonlinear activation functions, stacking multiple linear layers would still produce an overall linear transformation.

---

7. Python Implementation

A simple artificial neuron can be implemented using Python:

# Input values
inputs = [2, 3, 1]

# Corresponding weights
weights = [0.5, 0.8, 0.2]

# Bias
bias = 0.1

# Calculate weighted sum
z = sum(
    x * w for x, w in zip(inputs, weights)
) + bias

# ReLU activation
output = max(0, z)

print("Weighted Sum:", z)
print("Neuron Output:", output)

Expected output:

Weighted Sum: 3.2
Neuron Output: 3.2

This implementation demonstrates the forward computation of a single artificial neuron. It does not perform training or learn weights.

---

8. Key Takeaways

- Biological neurons inspired the conceptual design of artificial neurons.
- Dendrites receive information, while artificial neurons receive numerical inputs.
- Weights represent the influence of individual inputs.
- Bias adjusts the weighted sum.
- Activation functions determine the neuron's output.
- Neural networks learn by updating weights and biases during training.
- Multiple artificial neurons can be interconnected to form neural networks.

9. Conclusion

The journey from biological neurons to artificial neurons demonstrates how concepts from neuroscience inspired computational models.

A biological neuron processes electrochemical signals, while an artificial neuron performs mathematical computations. Despite their differences, both provide a useful framework for understanding how interconnected units can process information.

One biological neuron inspired a mathematical model. Millions of interconnected artificial neurons help power modern AI systems.

---

References for Further Learning

- "3Blue1Brown – But what is a neural network?" (https://www.3blue1brown.com/topics/neural-networks)
- "Google Machine Learning – Neural Networks" (https://developers.google.com/machine-learning/crash-course/neural-networks)
- "IBM – What are neural networks?" (https://www.ibm.com/think/topics/neural-networks)

---

Learning Notes | Artificial Intelligence & Machine Learning
Topic: Biological Neurons and Artificial Neurons