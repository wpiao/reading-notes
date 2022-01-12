# Retro 10: Stack and Queue - 01/11/2022

The implementation of Stack and Queue are same as in other programming language. I didn't have blockers. `Node` is the building block in the `Stack` and `Queue`. `Node` has `value` and `next` property. `Stack` has `top` property which refer to its top node. `Queue` has `front` property which refer to the front node and `rear` property which refer to the end node.

- `Stack` methods

  - `push`: push a node on the top of the `Stack`
  - `pop`: remove current top node and return its value
  - `peek`: return top node's value
  - `is_empty`: check if the stack is empty, return boolean

- `Queue` methods
  - `enqueue`: add a node in the front node of the `Queue`
  - `dequeue`: remove the front node and return its value
  - `peek`: return front node's value
  - `is_empty`: check if the queue is empty, return boolean
