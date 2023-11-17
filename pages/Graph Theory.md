# Graph
Non-empty set of vertices V with a set of two element subsets of V named set of edges E.
- ## Terms
	- ### Degree
	  Number of edges incident
	- ### Distance
	  The length of a shortest path between a given set of two vertices.
	- ### U-V Path
	  Path from U to V is a sequence which alternates between vertices and edges which starts and ends with a vertex. For an edge to be listed, the vertex one element prior and the following vertex must be adjacent.
	  
	  The length of a U-V path is the number of edges in the sequence.
		- #### Simple
		  A version of the U-V path in which no vertex is repeated.
	- ### Complete Graph
	  Every vertex has an edge to every other vertex
		- ### Complete Bipartile Graph Km,n
		  Vertices left column length m are connected to each vertex in right column n.
	- ### Multigraph
	  A graph allowing parallel edges and loops (denoted by lowercase Latin lettering)
		- #### Connected Graph
		  A multigraph that has a path to traverse from any vertex from given vertices U and V.
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
- ## Paths and Circuits