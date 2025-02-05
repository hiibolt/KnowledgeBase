## Anomalies
There are various potential anomalies that should be avoided.
	- ### Insertion Anomaly
	  When inserting a new record, it can create an *insertion anomaly* when you wish to insert but you are missing a primary key (or a part of the primary key tuple) for one reason or another.
	  
	  This is an anomaly because it violates the ((67a3dfa2-7699-493a-8df8-2c0f68c18b9e)) constraint.
	- ### Deletion Anomaly
	  When removing part of a record, it can create a *deletion anomaly* when you wish to delete in a manner that makes sense logically, but happens to remove part of all of a primary key.
	  
	  This is an anomaly because it also violates the ((67a3dfa2-7699-493a-8df8-2c0f68c18b9e)) constraint.
	- ### Update Anomaly
	  When updating some field that also has side effects on other similar fields for logical reasons, you are creating an *update anomaly*.
- ## Decomposition
  To solve or prevent these anomalies, we will approach our database design using a technique called *decomposition*. 
  
  This is where you break a logical record into more when you know or foresee some set of issues.
- ## Normalization
  Normalization is a more systematic method for ensuring database integrity and preventing issues before they surface.
	- ### Functional Dependencies
	  For a given set of attributes $X$ that uniquely identifies another set of attributes $Y$:
	  $$X \rarr Y$$
	  This is read as either:
	  * $X$ functionally determines $Y$
	  * $Y$ is functionally dependant on $X$
		- #### Armstrong's Axioms
		  $$\text{If }Y\subseteq X\text{ then }X\rarr$$
		  $$\text{If }X\rarr Y,\text{ then }XZ\rarr YZ\text{ for any }Z$$
		  $$\text{If }X\rarr Y\text{ and }Y\rarr Z\text{, then }X \rarr Z$$
		  $$\text{If }X\rarr YZ\text{ then }X\rarr Y\text{ and }X\rarr Z$$
		  $$\text{If }X\rarr Y\text{ and }A\rarr B\text{ then }XA\rarr YB$$
		  $$\text{If }X\rarr Y\text{ and }YZ\rarr W\text{ then }XZ\rarr W$$
		  $$I\rarr I\text{ for any }I$$