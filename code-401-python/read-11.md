# Read: 11 - NumPy - 01/15/2022

`NumPy` is a commonly used Python data analysis package.

```python
# Read csv file
import csv
with open("example.csv", "r") as f:
  examples = list(csv.reader(f, delimiter=";"))

# numpy array
import numpy as np
examples = np.array(examples[1:], dtype=np.float)

# check the number of rows and columns
examples.shape

# create an empty numpy array with all elements are 0
empty_array = np.zeros((3, 4))

# create an array with random numbers
np.random.rand(3, 4)

# Using numpy to read in files
np.genfromtxt("examples.csv", delimiter=";", skip_header=1)

# numpy array is zero-indexed
# get an element from numpy array
examples[row, column]
# slice numpy array
examples
examples[0:3,3]
```
