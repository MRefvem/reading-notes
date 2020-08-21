# Read:35 - Graphs

## Code Fellows reading: Graphs

A Graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.

Common terminology when working with Graphs include:
1. Vertex - A vertex, also called a "node", is a data object that can have zero or more adjacent vertices.
2. Edge - An edge is a connection between two nodes.
3. Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
4. Degree - The degree of a vertex is the number of edges connected to that vertex.

### Directed vs Undirected

#### Undirected Graphs

An Undirected Graph is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.

#### Directed Graphs (Digraph)

A Directed Graph also called a Digraph is a graph where every edge is directed. Unlike an undirected graph, a Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

### Complete vs Connected vs Disconnected

There are many different types of graphs. This depends on how connected the graphs are to other node/vertices.

#### Complete Graphs

A complete graph is when all nodes are connected to all other nodes.

#### Connected

A connected graph is a graph where all of the vertices/nodes have at least one edge. A tree is actually a form of a connected graph.

#### Disconnected

A disconnected graph is a graph where some vertices may not have edges. Some nodes may not always be connected to other nodes or vertices of a graph. Standalone nodes or edges are known as islands.

### Acyclic vs Cyclic

#### Acyclic Graph

An acyclic graph is a directed graph without cycles. A cycle is when a node can be traversed through and potentially end up back at itself. A directed acyclic graph is also called a DAG. This can be represented as what we know as a tree.

#### Cyclic Graphs

A cyclic graph is a graph that has cycles. A cycle is defined as a path of a positive length that starts and ends at the same vertex.

### Graph Representation

We represent graphs through 1. Adjacency Matrix and 2. Adjecency List.

#### Adjacency Matrix

An adjacency matrix is represented through a 2-dimensional array. If there are n vertices, then we are looking at an n x n Boolean matrix. Each row and column represents each vertex of the data structure. The elements of both the column and the row must add up to 1 if there is an edge that connects the two, or zero if there isn't a connection.

A sparse graph is where there are very few connections. A dense graph is where there are many connections.

Within an adjacency matrix, an undirected graph will always be symmetric. This is not the case for a directed graph.

#### Adjacency List

An adjacency list is the most common way to represent graphs. An adjacency list is a collection of linked lists or arrays that lists all of the other vertices that are connected. Adjacency lists make it easy to view if one vertices connects to another.

### Weighted Graphs

A weighted graph is a graph with numbers assigned to its edges. These numbers are called weights. When representing a weighted graph in a matrix, you set the element in the 2D array to represent the actual weight between the two paths. If there is not a connection between the two vertices, you can put a 0, although it is known for some people to put the infinity sign instead.

Within adjacency lists, you must include both the weight and the name of the adjacent vertex.

### Traversals

The traversal of a graph is similar to traversal methods for trees.

#### Breadth First

In a breadth first traversal, you are starting at a specific vertex/node.This node must be specified when calling the BreadthFirst() method. The breadth-first traversal of a graph is like that of a tree, with the exception that graphs can have cycles. When a graph has cycles and we are trying to traverse, this leaves the possiblity to create an infinite loop. To prevent an infinite loop, we need to have some sort of flag that specifies if we have already visited that vertices. Upon each visit, we just set the "visited" flag from false to true.

Breadth first traversal is when you visit all the nodes that are closest to the root as possible. From there you traverse outwards, level by level, until you have visited all the vertices/nodes.

The algorithm for the breadth-first traversal looks like:
1. Enqueue: the declared start node into the Queue.
2. Create a loop that will run while the node still has nodes present.
3. Dequeue: the first node from the queue.
4. If the dequeued node has unvisited child nodes, mark the unvisited children as visited and re-insert them back into the queue.

```
ALGORITHM BreadthFirst(vertex)
    DECLARE nodes <-- new List()
    DECLARE breadth <-- new Queue()
    breadth.Enqueue(vertex)

    while (breadth is not empty)
        DECLARE front <-- breadth.Dequeue()
        nodes.Add(front)

        for each child in front.Children
            if(child is not visited)
                child.Visited <-- true
                breadth.Enqueue(child)   

    return nodes;
```

A few things to remember about breadth-first traversals:
1. If there are any disconnected nodes (such as islands) with the graph data structure, they will not be traversed.
2. Breadth-first only outputs the nodes that are connected in some relation to the root that you pass in.

#### Depth First

In a depth first traversal, we approach it a bit different that the way we do when working with a depth first traversal of a tree. Similar to how the breadth-first uses a queue, we are going to use a stack for our depth-first traversal.

The algorithm for a depth first traversal is:

1. Push the root node into the stack.
2. Start a while loop while the stack is not empty.
3. Peek at the top node in the stack.
4. If the top node has unvisited children, mark the top node as visited, and then Push any unvisited children back into the stack.
5. If the top node does not have any unvisited children, Pop that node off the stack.
6. Repeat until the stack is empty.

### Real World Use of Graphs

Graphs are extremely popular when it comes to it's uses. Here are a few examples of graphs in use:

1. GPS and Mapping
2. Driving Directions
3. Social Networks
4. Airline Traffic
5. Netflix uses graphs for suggestions of 

