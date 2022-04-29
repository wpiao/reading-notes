# Retro:42 - Pythonisms - 04/28/2022

In python, we can implement `__iter__` method to make object iterable. By default, `Stack` is not iterable. I implemented `__iter__` method in `Stack` class to make `Stack` iterable.

```python
class Stack:
    def __init__(self, top=None):
        self.top = top

    def __iter__(self):
        def value_generator():
            current = self.top
            while current:
                yield current.value
                current = current.next
        return value_generator()
```

Example of Repeater class - iterable

```python
class Repeater:
  def __init__(self, value):
    self.value = value

  def __iter__(self):
    return self

  def __next__(self):
    return self.value
```
