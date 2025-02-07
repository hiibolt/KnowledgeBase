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
	  **Super_Type**($$\underline{SPR-ID}$$, SPR-attr)
	  **Sub_Type_1**($$\underline{SPR-ID}^t$$, ST-1-attr)
	  **Sub_Type_2**($$\underline{SPR-ID}^t$$, ST-2-attr)