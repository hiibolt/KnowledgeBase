## ER Diagrams
Stands for Entity-Relationship, which models the structure data by how they are related.
	- ### Entities
	  Principle (base) objects about which data is stored. 
	  
	  Can be considered a "thing" or a noun.
	  
	  Rendered as rectangles with inner text.
		- #### Weak Entities
		  These entities *depend* on the stronger entity.
		  
		  These are rendered as double-stroked rectangles - as must all associated relationships be.
	- ### Relationships
	  Connections between two entities.
	  
	  Can be thought of as a "descriptor".
	  
	  Rendered as a diamond with inner text, or a mini diamond with text outside.
		- #### Inheritance
			- #### "Is a" 
			  Is a *subtype* of a *supertype* (can be thought of as a base class).
			  
			  Rendered as an upside-down triangle.
			  
			  * **Generalization vs. Specialization**
			  Can you be the *supertype* without being a *subtype*? 
			  Yes, specialization. No, generalization (labelling).
			- #### "Is a part of"
			  Rendered as a triangle.
		- #### Degree
		  The number of entities associated with a relationship
		  
		  **Binary degree**: two associated entities
		  **Ternary degree**: three associated entities
		- #### Connectivity
		  Constrains a mapping. It's important to look at the minimum on the left, and the maximum on the right.
		  
		  It's possible to have optional relationships such as (0,m).
		  
		  * (1,1) = **one-to-one**
		  * (1,m) = **one-to-many**
		  * (m,m) = **many-to-many**
		  ...etc.
		- #### Recursive Relationships
		  Entities can be related to themselves.
		  
		  * Many to many - *Network*
		  * One to many - *Tree*
		  * One to one - *Chain*
	- ### Attributes
	  A *singular* piece of data attached to a relationship or entity.
	  
	  Attributes on relationships must be on a *many-to-many* relationship.
	  
	  Cannot be empty unless *explicitly* allowed to be.
	  
	  Two connecting lines signifies a multi-valued attribute.
	  
	  Rendered as a circle with inner text.
- ### Data Model Types
	- #### Relational
	  Data is stored in relations (tables), and each table has one sole entry.
	- #### Hierarchical
	  Stored in a tree format. An entry may have zero or many children.
	- #### Inverted List
	  Data is indexed via indices.
	- #### OO
	  Data is stored as objects.