# Read: 42 - Pythonisms - 04/25/2022

### Python Dunder Methods - Special Methods

- Object Initialization: `__init__`

  ```python
  class Account:
      """A simple account class"""

      def __init__(self, owner, amount=0):
          """
          This is the constructor that lets us create
          objects from this class
          """
          self.owner = owner
          self.amount = amount
          self._transactions = []
  ```

- Object Representation: `__str__`, `__repr__`

  1. `__repr__`: The "official" string representation of an object. This is how you would make an object of the class. The goal of `__repr__` is to be unambiguous.
  2. `__str__`: The "informal" or nicely printable string representation of an object. This is for the enduser.

  ```python
  class Account:
    # ... (see above)

    def __repr__(self):
        return 'Account({!r}, {!r})'.format(self.owner, self.amount)

    def __str__(self):
        return 'Account of {} with starting amount: {}'.format(
            self.owner, self.amount)

  ```

### Python Iterators

```python
class Repeater:
  def __init__(self, value):
    self.value = value

  def __iter__(self):
    return self

  def __next__(self):
    return self.value
```
