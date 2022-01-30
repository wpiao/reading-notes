# Read: 15 - Trees - 01/29/2022

### Terminology

- Node: it contain its own values, and references to other nodes
- Root: the node at the beginning of the tree
- k: a numter that specifies the maximum number of children any node may have in a tree. In a binary tree, k is 2
- Left: a reference to one child node, in a binary tree
- Right: a reference to the other child node, in a binary tree
- Edge: the edge in a tree is the link between a parent and child node
- Leaf: a leaf is a node that does not have any children
- Height: the height of a tree is the number of edges from the root to the furthest leaf

### Traversals

- Depth First

  - pre-order: root >> left >> right

    ```
    ALGORITHM pre_order(root)

      OUTPUT <-- root.value

      if root.left is not Null
      pre_order(root.left)

      if root.right is not Null
      pre_order(root.right)
    ```

  - in-order: left >> root > right

  ```
  ALGORITHM in_order(root)

    if root.left is not Null
      in_order(root.left)

    OUTPUT <-- root.value

    if root.right is not Null
      in_order(root.right)

  ```

  - post-order: left >> right >> root

  ```
  ALGORITHM post_order(root)

    if root.left is not Null
      post_order(root.left)

    if root.right is not Null
      post_order(root.right)

    OUTPUT <-- root.value
  ```

- Breadth First
- K-ary Trees
  If nodes are able to have more than 2 child nodes. k refers to the maximum number of children that each Node is able to have
