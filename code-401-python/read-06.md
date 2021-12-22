# Read: 06 - Game of Greed 1 - 12/21/2021

## Random module

```python
import random

# output random integer from 0 to 5
random.randint(0, 5)

# output random number from 0 to 5, not including 5
random.random() * 5

# shuffle
from random import shuffle
x = [i for i in range(10)]
shuffle(x)

# Generate a randomly selected element from range(start, stop, step)
random.randrange(start, stop[, step])
```

## Risk Analysis

Risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test.

- Possible risks
  - Use of new hardware
  - Use of new technology
  - Use of new automation tool
  - The sequence of code
  - Availability of test resources for the application
- Unavoidable risks
  - Time allocated for testing
  - A defect leakage due to the complexity or size of the application
  - Urgency from the clients to deliver the project
  - Imcomplete requirements
