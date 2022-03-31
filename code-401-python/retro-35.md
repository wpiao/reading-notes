# Retro:35 - Graph implementation - 03/30/2022

I was working on graph implementation. There are many ways to implement a graph and its `adjacency_list`.

```python
def __init__(self):
    self.adjacency_list = {}
    self.nodes = []
```

I add `nodes` property in the `__init__` method. When I add a node, I append that node to `nodes` property so that it is easier to implement `get_node` and `size` method.
