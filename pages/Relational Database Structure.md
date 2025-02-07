##  Relation Schema
In the form **Relation_Name**($A_1,A_2,\dots,A_N$), where $A_1, A_2, \dots, A_N$ are *attribute names*.

Each *attribute* becomes a **column**, and the *Relation_Name* becomes the **header**.
	- ### Tuples
	  A mathematical representation for the data in a database. They are **atomic**, meaning they *only allow one value*.
	- ### Degree
	  The number of attributes present (including any keys).
	- ### Cardinality
	  The number of tuples present.
- ## Keys
	- ### Super Key
	  An attribute or set of attributes that *uniquely identify* a tuple within a relation.
		- ### Candidate Key
		  The *minimal set of attributes* necessary to uniquely identify a tuple within a relation. *There can be multiple*.
	- ### Primary Key
	  The final discriminator for uniquely referencing tuples in a given relation.
	  
	  Rendered in the tuple by underlining:
	  \begin{equation}\textbf{Relation\_Name}(\underline{A_1},\underline{A_2},A_3,\dots,A_N)\end{equation}
	- ### Foreign Key
	  id:: 67a3dd0f-27ee-4a5c-8a49-58b13acb6f14
	  Points to a unique tuple in a another relation - labeled the *home relation*.
- ## Attributes
  It's worth nothing that attributes do not need to be sorted. As long that two tuples have schemas have the same *name*, *attributes*, and *primary key*, they are equivalent - a property known as *order independence*.
	- ### Domain
		- #### Single Attribute
		  All possible values of a given attribute.
		- #### Set of Attributes
		  All possible combinations of all possible values of a given attribute.
- ## Constraints
  A *constraint* is a limit imposed on the domain of an attribute.
	- ### Entity Integrity
	  id:: 67a3dfa2-7699-493a-8df8-2c0f68c18b9e
	  One common example is the *entity integrity* constraint, which simply states that the primary key of an entity must be **non-null**.
	- ### Referential Integrity
	  A second common example is the *referential integrity* constraint, which states that while a foreign key may or may not be null, it *cannot* point to an invalid or non-existent primary key - that is, a key that does not have a matching schema with it as its primary key.