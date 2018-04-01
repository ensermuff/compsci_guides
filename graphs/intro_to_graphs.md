# Graphs
## Introduction

Graphs are one of the most prevalent data structures in computer science. It's a powerful data structure that's utilized to represent relationships between different types of data. In a graph, each data point is stored as a **node** and each relationship between those data points is represented by an **edge**. For example, a social network is considered a graph in which each person is considered a node and a friendship between two people is considered an edge.

For interviews, it is vital to know how to implement a graph, basic graph traversals (BFS, DFS) and how to topologically sort the graph.



## Graph Terminology
### Graph components
Graphs consist of a set of..
* **vertices**, which are also referred to as nodes
    * Nodes that are directly connected by an edge are commonly referred to as **neighbors**.
* **edges**, connections between pairs of vertices

**![](https://lh4.googleusercontent.com/k-g2IQwT-LzoLAlxjvNdw-J4_FAOdKgq_YHTOgV36ku2oKCKpGIT_gU3lRGvsokF2zhXtss-hK7xNjD_xPguZlzMMHr6JDwxZkEwkjO6_aDI59DjJg15Zk0TDbIIlb5QazloMtJFHig)**


### Graph types

#### Directed & undirected graphs
A **directed** graph is a graph that in which all edges are associated with a direction. An example of a directed edge would be a one way street.

An **undirected** graph is a graph in which all edges do not have a direction. An example of this would be a friendship!

<img src="https://github.com/codepath/compsci_guides/blob/graphs/graphs/figures/directed_undirected_graph.png" width="486" height="380"/>

#### Cyclic & acyclic graphs
Before going over the what cyclic and acyclic graphs are, there are two key terms to cover: **path** and **cycle**. A **path** is a sequence of vertices connected by edges and a **cycle**  a path whose first and last vertices are the same.

A **cyclic** graph means that there contains a least one cycle within the graph.

An **acyclic** graph has no cycles within it.

<img src="https://github.com/codepath/compsci_guides/blob/graphs/graphs/figures/acyclic_cyclic_graph.png" width="486" height="380"/>

A commonly used phrase when referring to graphs is a **directed acylic graph (DAG)**, which is a directed graph in which there are *no* cycles. In a DAG, these two terms are commonly used to denote nodes with special properties:
* **Sink** nodes have no outgoing edges, only incoming edges
* **Source** nodes only have outgoing edges, no incoming edges

## Graph representations
### Adjacency lists
**Adjacency list** is the most common way to represent graphs. With this approach of representing a graph, each node stores a list of its adjacent vertices. For undirected graphs, each edge from _u_ to _v_ would be stored twice: once in _u_'s list of neighbors and once in _v_'s list of neighbors.

<img src="https://github.com/codepath/compsci_guides/blob/graphs/graphs/figures/adjacency_list_graph.png" width="755" height="350"/>

### Edge sets/ lists
An **edge set** simply represents a graph as a collection of all its edges.

<img src="https://github.com/codepath/compsci_guides/blob/graphs/graphs/figures/edge_set_graph.png" width="755" height="350"/>


### Adjacency matrix
An **adjacency matrix** represents a graph with _n_ nodes as a _n_ by _n_ boolean matrix, in which matrix[_u_][_v_] is set to true if an edge exists from node _u_ to node _v_.

<img src="https://github.com/codepath/compsci_guides/blob/graphs/graphs/figures/adjacency_matrix_graph.png" width="685" height="350"/>

The representation of a graph is efficient for checking if an edge exists between a pair of vertices. However, it may be less efficient for search algorithms because it requires iterating through all the nodes in the graph to identify a node's neighbors.

### Runtime Analysis


|  Representation       | Column 2 | Traversing entire graph | hasEdge(u, v) | Space    |
| --------              | -------- | --------                | --------      | -------- |
| **Adjacency matrix**  | Text     | O(V<sup>2</sup>)        | O(1)          | O(V<sup>2</sup>)|
| **Edge Set**          | Text     | O(E)                    | O(E)          | O(E)
| **Adjacency List**    | Text     | O(V + E)                | O(max number of edges a vertex has)  | O(E + V)
Credit: [UC Berkeley data structures course](https://docs.google.com/presentation/d/1GOOt1Ierm9jJFq9o26uRW20GdU6E5hrAZvsoQIreJew)


**Example interview question using topological sorting:**
## Glossary
1. **vertex (a.k.a. node):** used to represent one data point
2. **edge:** connections between pairs of vertices
3. **neighbor:** a neighbor node refers to a node that is directly connected to another node by an edge
4. **directed graph:** a graph that in which all edges are associated with a direction
5. **undirected graph:** a graph that in which all edges have no directions
6. **path:** is a sequence of vertices connected by edges
7. **cycle:**  a path whose first and last vertices are the same
8. **cyclic graph:** a graph in which at least one cycle exists
9. **acyclic graph:** a graph in which no cycle exists
10. **adjacency list:** an approach to represent graphs in which each node stores a list of its adjacent vertices
11. **edge set/list:** an approach to represent graphs in which a graph as a collection of all its edges
12. **adjacency matrix:** an approach to represent graphs in which graph with _n_ nodes as a _n_ by _n_ boolean matrix, in which matrix\[_u_\]\[_v_\] is set to true if an edge exists from node _u_ to node _v_.
13. **breadth first search:** pick an arbitrary node as the root and explore each of its neighbors before visiting their children
14. **depth first search:** start with an arbitrary node as a root and explore each neighbor fully before exploring the next one
15. **topological sort:** an ordering of nodes for a directed acyclic graph (DAG) such that for every directed edge _uv_ from vertex _u_ to vertex _v_, _u_ comes before _v_ in the ordering.
16. **sink nodes:** in a DAG, a sink node has no outgoing edges
17. **source nodes:** in a DAG, a source node only has outgoing edges
18. **directed acylic graph (DAG):** a directed graph in which there are *no* cycles


## Extra graph algorithms
**NOTE**: This section covers algorithms that will generally not come up in interviews.
#### Union find, disjoint sets

#### Shortest paths algorithms

#### Minimum spanning tree algorithms
