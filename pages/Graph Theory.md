# Graph
Non-empty set of vertices V with a set of two element subsets of V named set of edges E.
	- ## Directed Graph
	  Edges have directions.
	- ### Multigraph
	  A graph allowing parallel edges and loops (denoted by lowercase Latin lettering)
		- #### Connected Graph
		  A multigraph that has a path to traverse from any vertex from given vertices U and V.
- ## Terms
	- ### Degree
	  Number of edges incident
	  * Indegree: Degree of directional edges into a given vertice
	  * Outdegree: Degree of directional edges out from a given vertice
	- ### Distance
	  The length of a shortest path (least # of edges) between a given set of two vertices.
		- ## Breadth-First Search Algorithm
		  *Note: Professor wants alphabetical selection for next vertice.*
	- ### Path *(U-V definition)*
	  Path from U to V is a sequence which alternates between vertices and edges which starts and ends with a vertex. For an edge to be listed, the vertex one element prior and the following vertex must be adjacent.
	  
	  The length of a U-V path is the number of edges in the sequence.
		- ### Simple
		  A version of the U-V path in which no vertex is repeated.
		- ### Cycle
		  A U-V path that leads back to U.
			- ### Tree
			  A *connected* graph with no cycles.
			  * There is a unique simple path between any two vertices
			  * Always **n + 1** vertices compared to **n** edges.
			  * A vertex is either 'internal' if it has children or a 'leaf' / 'terminal vertex'
				- ### Spanning Tree
				  A connected graph turned into a tree using only edges.
				- ### Rooted Tree
				  A directed graph with a unique vertex with an indegree of zero and all other vertices having an indegree of 1.
					- ### Binary Tree
	- ### Complete Graph
	  Every vertex has an edge to every other vertex
		- ### Complete Bipartile Graph Km,n
		  Vertices left column length m are connected to each vertex in right column n.
	- ### Loop
	  An edge which connects a node to itself. There contribute 2 to the degree of a vertex versus one.
	- ### Parallel Edge
	  An edge which connects two points that are already connected by another edge
	- ### Isomorphism
	  A function that proves two graphs have the same shape
	  
	  Defined as a bijection such that Vertices X and Y of G are adjacent if and only if vertices f(X) and f(Y) are adjacent it H.
		- #### Tactic 1 for checking against isomorphism:
		  Count the number of vertices
		- #### Tactic 2 for checking against isomorphism:
		  List of the degrees of the vertices in ascending or descending order
- ## Theorems
	- ### Handshaking Theorem
	  $\sum{degree} = 2* n_{edges}$
- ## Representations
	- ### Adjacency Lists
	  $P_1 : P_2, P_3, ...$
	  $P_2 : P_3, ...$
	- ### Adjacency Matrices
	  |  | P_1 | P_2 |
	  | P_1 | 0 | 1 |
	  | P_2 | 1 | 0 |
	  **Note: Multiple adjacencies to a node or itself increments the count on the matrix accordingly**
	  **Note: In the case of a directed graph, the row is X and the column is Y**
- ## Search Algorithmns
	- ## Depth-First Search
	  * today in your MWF 1PM classStart with A
	  * Label it 1 (-)
	  * Every new vertex has a number one higher than the last vertext.
	  * Use the lowest letter first if there is no clear number