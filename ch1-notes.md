Network:

```python
class Network(object):
  def __init__(self, sizes):
    self.num_layers = len(sizes)
    self.sizes = sizes
    # Random init biases for each non-input later.
    self.biases = [np.random.rand(y, 1)] for y in sizes[1:]
    # Rand weights for each non-input unit from each previous layer unit.
    self.weights = [np.random.rand(y, x)] for x, y in zip(sizes[:-1], sizes[1:])

# Create network with 2 input, 3 hidden (L2), 1 output
net = Network([2, 3, 1])
```

Notation: w_jk = weight from jth unit in L2 (hidden) to kth in L3 (output)
Thus activation of L3 is
a' = sigma(wa + b)
