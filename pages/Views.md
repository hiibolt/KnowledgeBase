## View
A view is a virtual table which derives data from other tables (or views!) via a query that is a part of its definition.

They are *virtual* - meaning that they don't contain their own data.
	- ### Advantages
	  * Simply user's otherwise complicated [[DML]] operations 
	  * Users can be denied base tables for additional security
- ## Creation
  ```SQL
  CREATE VIEW <view_name>
  	[( <view_col_name> [, <view_col_name>]...)] # Used to rename columns
      AS SELECT <attr_name> [, <attr_NAME>] ...
      	FROM <source_table_or_view> [, ...]
      	WHERE <condition>;
  ```
	- ### Example 1
	  ```SQL
	  CREATE VIEW Dekalb_People
	  	(SSN, first_name, last_name) # Renames tuple columns
	      AS SELECT SSN, FNAME, LNAME
	      	FROM Person
	          WHERE ZIP = '60115';
	  ```
	- ### Example 2
	  ```SQL
	  CREATE VIEW grade_tally
	  	(grade, howmany)
	      AS SELECT grade, COUNT(*)
	      	FROM transcript
	          GROUP BY grade;
	  ```
- ## Dropping
  ```SQL
  DROP VIEW <view_name>;
  ```