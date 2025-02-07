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
	  **Sub_Type_1**($$\underline{\text{SPR-ID}}^t$$, ST-1-attr)
	  **Sub_Type_2**($$\underline{\text{SPR-ID}}^t$$, ST-2-attr)
	- ### Weak Entity
	  Given a weak entity *WE* that relies on a strong entity *SE*, you *must* include the SE's identifier as a part of the primary key.
	  
	  For example:
	  **Strong_Entity**($$\underline{\text{SE-ID}}$$, SE-attr)
	  **Weak_Entity**($$\underline{\text{SE-ID}}$$, $$\underline{\text{WE-ID}}$$, WE-attr)