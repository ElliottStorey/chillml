# Chill ML

A simple neural network framework built from scratch in Python.

## Getting Started

### Installation

Clone the repository:

```bash
git clone https://github.com/ElliottStorey/chillml.git
cd chillml
```

### Usage

Create a simple neural network:

```python
from chillml import Network
from chillml.layers import FullyConnected
from chillml.losses import MeanSquaredError
import numpy as np

# Define layers
layers = [
    FullyConnected(4, 1)
]

# Create network
network = Network(layers, MeanSquaredError)

# Train
network.train(training_inputs, training_outputs, 75, 0.01)

# Predict
prediction = network.forward(test_input)
```

See the [examples](examples/) folder for complete examples including:
- `squares.py` - Simple square averaging example
- `mnist.py` - MNIST digit classification

## Features

### Layers
* Fully Connected (Dense) layers

### Loss Functions
* Mean Squared Error
* Binary Cross Entropy

### Activation Functions
* ReLU
* Sigmoid
* Softmax
* Tanh (Hyperbolic Tangent)
