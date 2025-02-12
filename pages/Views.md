## View
A view is a virtual table which derives data from other tables (or views!) via a query that is a part of its definition.

They are *virtual* - meaning that they don't contain their own data.
- ## Creation
  ```SQL
  CREATE VIEW <view_name>
  	[( <view_col_name> [, <view_col_name>]...)] # Used to rename columns
      AS SELECT <attr_name> [, <attr_NAME>] ...
      	FROM <source_table_or_view> [, ...]
      	WHERE <condition>;
  ```
	- ### Example
	  ```SQL
	  CREATE VIEW Dekalb_People
	  	(SSN, first_name, last_name) # Renames tuple columns
	      AS SELECT SSN, FNAME, LNAME
	      	FROM Person
	          WHERE ZIP = '60115';
	  ```