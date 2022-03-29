# Read:35 - Graph - 03/28/2022

### Terminologies

1. Graph: a collection of `vertices or nodes` potentially connected by line segments named `edges`
2. Vertex: a data object that can have zero or more adjancent vertices
3. Edge: a connection between two nodes
4. Neighbor: adjacent vertices/nodes
5. Degree: number of edges connected to that vertex.

### Graph Representation

1. Adjancency Matrix: a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matirx
2. Adjacency List: a collection of linked lists or array that lists all of the other vertices that are connected

### Traversals

1. Breadth First

   - Enqueue the declared start node into the Queue.
   - Create a loop that will run while the node still has nodes present.
   - Dequeue the first node from the queue
   - if the Dequeue‘d node has unvisited child nodes, add the unvisited children to visited set and insert them into the queue.

2. Depth First
   - Push the root node into the stack
   - Start a while loop while the stack is not empty
   - Peek at the top node in the stack
   - If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
   - If the top node does not have any unvisited children, Pop that node off the stack
   - repeat until the stack is empty.

### Real world uses of Graph

1. GPS and Mapping
2. Driving Directions
3. Social Networks
4. Airline Traffic
5. Netflix uses graphs for suggestions of products

### References

[Graph](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-35/resources/graphs.html)
