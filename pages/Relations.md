## Ordered Pair
An ordered pair $( a, b )$ becomes 
$$\{\{a\}\text{, }\{a,b\}\}$$
- ### Cartesian Product
  A * B = {(a, b): a $$\epsilon$$A and b $$\epsilon$$ B}
  
  Example: A = {1, 2}, B = {3, 4, d}
  * A x B = {(1, 3), (1, 4), (1, d), (2, 3), (2, 4), (2, d)}
- ## Relation
  Given sets A and B, relation R from A to B \subset of the Cartesian Product of A * B.
  
  A relation on a set S is a relation from S to S.
  
  To find all relations from C to D, list all subsets of A * B.
  
  The number of relations is $$2^{|A|*|B|}$$.
	- ### Notation
	  If (x, y) \epsilon R, then xRy.
	- #### Reflexive Property
	  If for every element in A the relation has (e, e), it is reflexive.
	- #### Symmetric Property
	  If, for (y, x) \epsilon R, there is (x ,y), relation R is symmetrical.
	- #### Transitive Property
	  If xRy and yRz implies xRz. Check for cases where not xRz.
	- ### Equivalence Relation
	  id:: 6508b564-f18f-4d56-aa4a-3430136636db
	  A relation R is only an equivalence relation if it is reflexive, symmetric, and transitive
- ## Partition
  A collection of subsets where 
  S = $$A_u \bigcup A_2 \bigcup ... \bigcup A_n$$
  $A_i \bigcap A_j = \{\}$
  $A_i =/ \{\}$
	- ### Partitions vs ((6508b564-f18f-4d56-aa4a-3430136636db))
	  A partition has an according equivalence relation, and an equivalence relation creates a partition