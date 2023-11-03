# Graph
Non-empty set of vertices V with a set of two element subsets of V named set of edges E.
- ## Terms
	- ### Degree
	  Number of edges incident
	- ### Complete Graph
	  Every vertex has an edge to every other vertex
		- ### Complete Bipartile Graph Km,n
		  Vertices left column length m are connected to each vertex in right column n.
	- ### Isomorphism
	  A function that proves two graphs have the same shape
	  
	  Defined as a bijection such that Vertices X and Y of G are adjacent if and only if vertices f(X) and f(Y) are adjacent it H.
- ## Theorems
	- ### Handshaking Theorem
	  $\sum{degree} = 2* n_{edges}$
- ## Representations
	- ### Adjacency Lists
	  $P_1 : P_2, P_3, ...$
	  $P_2 : P_3, ...$
	- ### Adjacency Graphs
	  |  | P_1 | P_2 |
	  | P_1 | 0 | 1 |
	  | P_2 | 1 | 0 |