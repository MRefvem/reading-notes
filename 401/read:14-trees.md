# Read:14 - Trees

## Code Fellows Tutorial: Trees

### Common Terminology
- Node - a node is the individual item/data that makes up the data structure
- Root - The root is the first/top node in the tree
- Left Child - The node that is positioned to the left of a root or node
- Right Child - The node that is positioned to the right of a root or node
- Edge - The edge in a tree is the link between a parent and child node
- Leaf - A leaf is a node that does not contain any children
- Height - The height of a tree is determined by the number of edges from the root to the bottommost node

### Traversals

An important aspect of trees is how to traverse them. Traversing a tree allows us to search for a node, print out the contents of a tree, and much more. There are two categories of traversals.

- Depth first
Depth first is where we prioritize going through the depth (height) of the tree first.
- Breadth First
Breadth first traversal iterates through the tree by going through each level of the node-by-node.

### Binary Trees

Trees can have any number of children per node, but Binary Trees restrict the number of children to two. There is no specific sorting order for a binary tree. Nodes can be added into a binary tree wherever space allows.

The big O time complexity for inserting a new node is O(n). Searching for a specific node will also be O(n). Because of a lack of organizational structure in a Binary Tree, the worst case for most operations will involve traversing the entire tree.

The Big O space complexity for a node insertion using breadth first insertion will be O(w). Where w is the largest width of the tree.