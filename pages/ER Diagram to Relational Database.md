## Entities
Entities will become relations. How they do so varies on the type!
	- ### Strong Entity With No Sub-type
	  The primary key becomes all of the identifying attributes. All other attributes are placed into the final tuple.
	- ### Strong Entity With Sub-type
	  There are two ways to do this for a strong super type entity *SPR* with sub types *ST-1* and *ST-2*. 
	  
	  **Method 1**:
	  You can place them all in one record:
	  |<ins>SPR-ID</ins>|SPR-attr|ST-type|ST-1-attr|ST-2-attr|
	  
	  **Method 2**:
	  You can place them into three different relations:
	  **Super_Type**($$\underline{\text{SPR-ID}}$$, SPR-attr)
	  **Sub_Type_1**($$\underline{\text{SPR-ID}}^\dagger$$, ST-1-attr)
	  **Sub_Type_2**($$\underline{\text{SPR-ID}}^\dagger$$, ST-2-attr)
	- ### Weak Entity
	  Given a weak entity *WE* that relies on a strong entity *SE*, you *must* include the SE's identifier as a part of the primary key.
	  
	  For example:
	  **Strong_Entity**($$\underline{\text{SE-ID}}$$, SE-attr)
	  **Weak_Entity**($$\underline{\text{SE-ID}}^\dagger$$, $$\underline{\text{WE-ID}}$$, WE-attr)
- ## Relationships
	- ### Binary
		- #### One-to-One (O2O)
		  For two entities *A* and *B*, you can simply assign ((67a3dd0f-27ee-4a5c-8a49-58b13acb6f14))s to either tuple to represent the pairing:
		  
		  **Entity_A**($$\underline{\text{A-ID}}$$,A-attr,$$\text{B-ID}^\dagger$$)
		  ...xor...
		  **Entity_B**($$\underline{\text{B-ID}}$$,B-attr,$$\text{A-ID}^\dagger$$)
		  
		  This implies two functional dependancies:
		  $$A\rarr B$$
		  $$B\rarr A$$
		- #### One-to-Many (O2M)
		  For an entity *A* with relations to many *B*s, but each *B* only has one *A*, you can assign a foreign key pointing to *A* into *B*'s tuple. For example:
		  
		  **Entity_B**($$\underline{\text{B-ID}},B-attr,\text{A-ID}^\dagger)$$
		  
		  This implies one functional dependancy:
		  $$B\rarr A$$
		- #### Many-to-Many (M2M)
		  For an entity **A** and **B**, where **A** can have many connections to **B**s, and vice versa, you must create an *intersection table*:
		  
		  **Entity_A**($$\underline{\text{A-ID}}$$, A-attr)
		  **Entity_B**($$\underline{\text{B-ID}}$$, B-attr)
		  **A_B_Intersection**($$\underline{\text{A-ID}}^\dagger$$, $$\underline{\text{B-ID}}^\dagger$$)
		  
		  *Note*:
		  For certain M2M relationships, you should specify whether a link is *directed* or *un-directed*, as this would change whether ($$\underline{\text{A-ID}}^\dagger$$, $$\underline{\text{B-ID}}^\dagger$$) implies ($$\underline{\text{B-ID}}^\dagger$$, $$\underline{\text{A-ID}}^\dagger$$). Directed implies **no**, un-directed implies **yes**.
	- ### Non-Binary
	  All require a new intersection table, but how many potential options largely depends on how many *one-legs* you have.
	  
	  For example, for a ternary relationship with entities *A*, *B*, and *C*, and **three** *one-legs*:
	  |Functional Dependancy|Potential Relationship|
	  |$$A,B\rarr C$$|**A_B_to_C**($$\underline{\text{A-ID}}^\dagger$$, $$\underline{\text{B-ID}}^\dagger$$, $$\text{C-ID}^\dagger$$)|
	  |$$B,C\rarr A$$|**B_C_to_A**($$\underline{\text{B-ID}}^\dagger$$, $$\underline{\text{C-ID}}^\dagger$$, $$\text{A-ID}^\dagger$$)|
	  |$$C,A\rarr B$$|**C_A_to_B**($$\underline{\text{C-ID}}^\dagger$$, $$\underline{\text{A-ID}}^\dagger$$, $$\text{B-ID}^\dagger$$)|
	  
	  **Two One-Legs A and B**:
	  |Functional Dependancy|Potential Relationship|
	  |$$A,C\rarr B$$|**A_C_to_B**($$\underline{\text{A-ID}}^\dagger$$, $$\underline{\text{C-ID}}^\dagger$$, $$\text{B-ID}^\dagger$$)|
	  |$$B,C\rarr A$$|**B_C_to_A**($$\underline{\text{B-ID}}^\dagger$$, $$\underline{\text{C-ID}}^\dagger$$, $$\text{A-ID}^\dagger$$)|
	  
	  **One One-Legs, A**:
	  |Functional Dependancy|Relationship|
	  |$$B,C\rarr A$$|**B_C_to_A**($$\underline{\text{B-ID}}^\dagger$$, $$\underline{\text{C-ID}}^\dagger$$, $$\text{A-ID}^\dagger$$)|
	  
	  **No One-Legs**:
	  |Functional Dependancy|Potential Relationship|
	  |None|**A_B_C_Relationship**($$\underline{\text{A-ID}}^\dagger$$, $$\underline{\text{B-ID}}^\dagger$$, $$\underline{\text{C-ID}}^\dagger$$)|