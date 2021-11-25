# class 35 Reading Notes:Graphs
# Graphs

![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/undirectedgraph.png)
 - A graph is a non-linear data structure that can be looked at as a collection of vertices (or nodes) potentially connected by line segments named edges.


- terminology used when working with Graphs:

1. Vertex - A vertex, also called a “node”, is a data object that can have zero or more adjacent vertices.
2. Edge - An edge is a connection between two nodes.
3. Neighbor - The neighbors of a node are its adjacent nodes, i.e., are connected via an edge.
4. Degree - The degree of a vertex is the number of edges connected to that vertex.

# Directed vs Undirected:

![](https://www.differencebetween.com/wp-content/uploads/2011/05/DifferenceBetween_Directed_UnDirected_Graphs1.jpg)

1. Undirected Graphs :  is a graph where each edge is undirected or bi-directional. This means that the undirected graph does not move in any direction.


2. Directed Graphs:  also called a Digraph is a graph where every edge is directed.
- Digraph has direction. Each node is directed at another node with a specific requirement of what node should be referenced next.

## Complete vs Connected vs Disconnected:

![](https://media.cheggcdn.com/media/546/546deafc-f763-4250-9f15-d600fa22e55a/phpOZYHkz.png)

- Complete Graphs : A complete graph is when all nodes are connected to all other nodes.

- Connected : A connected graph is graph that has all of vertices/nodes have at least one edge.

- Disconnected : A disconnected graph is a graph where some vertices may not have edges.

## Acyclic vs Cyclic:

![](https://www.researchgate.net/profile/Elisa-Bertino/publication/2431833/figure/fig2/AS:339592545882121@1457976580886/Example-of-cyclic-and-acyclic-graphs.png)

- Acyclic Graph : is a directed graph without cycles.

 - (A cycle is when a node can be traversed through and potentially end up back at itself). 

- Cyclic Graphs : is a graph that has cycles.

- (A cycle is defined as a path of a positive length that starts and ends at the same vertex).

## Graph Representation
1. Adjacency Matrix: 

- An Adjacency matrix is represented through a 2-dimensional array. If there are n vertices.

2. Adjacency List

- An adjacency list is a collection of linked lists or array that lists all of the other vertices that are connected.


- Weighted Graphs : is a graph with numbers assigned to its edges. 

### Weighted Graphs: 
- is  numbers assigned to its edges. These numbers are called weights.

## Traversals

1. Breadth First

![](https://i.ytimg.com/vi/QRq6p9s8NVg/maxresdefault.jpg)

2. Depth First: 

![](https://i.ytimg.com/vi/iaBEKo5sM7w/maxresdefault.jpg)

## Real World Uses of Graphs:

- Examples of graphs in use:
  
  1. GPS and Mapping
  2. Driving Directions
  3. Social Networks
  4. Airline Traffic
  5. Netflix uses graphs for suggestions of products