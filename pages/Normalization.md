## Anomalies
There are various potential anomalies that should be avoided.
	- ### Insertion Anomalies
	  When inserting a new record, it can create an *insertion anomaly* when you wish to insert but you are missing a primary key (or a part of the primary key tuple) for one reason or another.
	  
	  This is an anomaly because it violates the ((67a3dfa2-7699-493a-8df8-2c0f68c18b9e)) constraint.
	- ### Deletion Anomalies
	  When removing part of a record, it can create a *deletion anomaly* when you wish to delete in a manner that makes sense logically, but happens to remove part or all of a primary key.
	  
	  This is an anomaly because it also violates the ((67a3dfa2-7699-493a-8df8-2c0f68c18b9e)) constraint.
	- ### Update Anomalies
	  id:: 67a3e009-9b2a-4130-8d24-d756071d5806
	  When updating some field that also has side effects on other similar fields for logical reasons, you are creating an *update anomaly*.
- ## Decomposition
  To solve or prevent these anomalies, we will approach our database design using a technique called *decomposition*. 
  
  This is where you break a logical record into more when you know or foresee some set of issues.
- ### Functional Dependencies
  For a given set of attributes $X$ that uniquely identifies another set of attributes $Y$:
  $$X \rarr Y$$
  This is read as either:
  * $X$ functionally determines $Y$
  * $Y$ is functionally dependant on $X$
	- ### Armstrong's Axioms
	  $$\text{If }Y\subseteq X\text{ then }X\rarr Y$$
	  $$\text{If }X\rarr Y,\text{ then }XZ\rarr YZ\text{ for any }Z$$
	  $$\text{If }X\rarr Y\text{ and }Y\rarr Z\text{, then }X \rarr Z$$
	  $$\text{If }X\rarr YZ\text{ then }X\rarr Y\text{ and }X\rarr Z$$
	  $$\text{If }X\rarr Y\text{ and }A\rarr B\text{ then }XA\rarr YB$$
	  $$\text{If }X\rarr Y\text{ and }YZ\rarr W\text{ then }XZ\rarr W$$
	  $$I\rarr I\text{ for any }I$$
	- ### In Schema
	  \begin{equation}\textbf{R}(\underline{a},b,c,d,e,f) = a\rarr a, b, c, d, e , f\end{equation}
- ## Normalization
  Normalization is a more systematic method for ensuring database integrity and preventing issues before they surface.
	- ### First Normal Form (1NF)
	  The sole requirement for the *first normal form* is that the database must be **atomic** (only one entry per field).
	  
	  This is achieved by duplicating records - which will likely introduce one or more ((67a3e009-9b2a-4130-8d24-d756071d5806)). However, this is okay - the next forms will patch any such issues out.
	- ### Second Normal Form (2NF)
	  The requirement for the *second normal form* is that the database must have no functional dependencies, that being, for the LHS (primary key) $X$ and RHS $Y$:
	  $$X\rarr Y$$
	  $$\text{and}$$
	  $$\text{No }\subset X\text{ determines }Y$$
	  
	  In other words, for each **FD**, the LHS must be the *entire* primary key and cannot be a part of it.
	  
	  Given a violating **FD**, split the RHS into its own relation with the LHS as the primary key.
	- ### Third Normal Form (3NF)
	  Finally, we must address any remaining **FD**s of which the LHS is not a prime - in other words, which are not relations at this point.
	  
	  As with the past forms, we then *decompose* further.