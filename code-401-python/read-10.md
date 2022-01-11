# Read: 10 - Stacks and Queues - 01/10/2022

## Stacks

- It consists of `Nodes`. Each `Node` references the next `Node` in the stack.
- Analogy: Stacks plates. When it comes to use plate, you use the one on the top, which is the one you stacked last.
- FILO: First In Last Out or LIFO: Last In First Out
- Common methods:
  - `push`: Node that is put into the top of the stack. O(1)
  - `pop`: Node that are removed from the top of the stack. O(1)
  - `top`: Top of the stack.
  - `peek`: View the value of the top Node. If the stack is empty, `peek` would raise an exception. O(1)
  - `isEmpty`: See if the stack is empty, return boolean. O(1)

## Queues

- Analogy: Form a waiting line. The person in the first of the line will be taken care of.
- FIFO: First In First Out or LILO: Last In Last Out
- Common methods:
  - `enqueue`: Add a `Node` to the rear. O(1)
  - `dequeue`: Remove the `Node` from the rear. O(1)
  - `peek`: peek the front node value. O(1)
  - `isEmpty`: See if the Queue is empty, return boolean. O(1)
