## Insertion
*[Docs](https://mariadb.com/kb/en/insert/)*

There are multiple options for insertion syntax:
```SQL
INSERT INTO <table_name>
VALUES (<value_list>);
```
...note the lack of attribute list!

With an attribute list:
```SQL
INSERT INTO <table_name>
(<attr_list>)
VALUES (<value_list>);
```
...note that both of these options require pre-determined values.

For variadic queries:
```SQL
INSERT INTO <table_name>
<another_query>;
```
	- ### Example 1
	  ```SQL
	  INSERT INTO Person
	  	Values('123456789',
	            'Inigo',
	            'Montoya',
	            '555555555555'
	            );
	  ```
	- ### Example 2
	  ```SQL
	  INSERT INTO Person
	  	(LNAME,FNAME,SSN)
	      Values('Inigo',
	            'Montoya',
	            '123456789'
	            );
	  ```
- ## Updating
  Allows you to update one or more rows.
  
  ```SQL
  UPDATE <table_name>
  	SET <attr> = <value> [, <attr> = <value> ...]
      [ WHERE <expression> ];
  ```
	- ### Example 1
	  This would update *everybody* to the following:
	  ```SQL
	  UPDATE Person
	  	SET FNAME='Spartacus'
	      	LNAME=''
	          PHONE='';
	  ```
	- ### Example 2
	  ```SQL
	  UPDATE Student
	  	SET CLSYEAR = 'Senior'
	      WHERE TOTALHRS > 90;
	  ```
	- ### Example 3
	  ```SQL
	  UPDATE Student
	  	SET GPA = 4.000
	      WHERE SSN='9999999999';
	  ```
- ## Deletion
  ```SQL
  DELETE FROM <table_name> [ WHERE <expression> ];
  ```
	- ### Example
	  Deletes every `Person`
	  ```SQL
	  DELETE FROM Person;
	  ```
	-
- ## Selection
  See ((67b3ab81-e18b-4fd4-9570-402e058cf68a)).
	- ## Multiple Tables
	  Selecting from two different tables is the ((67b3ab81-2888-4a43-a9fe-9336dc72ada4)) of the table's values.
	  ```SQL
	  SELECT DISTINCT P, CITY
	  	FROM SP, S
	      WHERE SP.S = S.S;
	  ```
	- ## `WHERE` Clause
	  Useful for specifying which rows to affect - commonly used with `UPDATE` and `SELECT` commands.
	  
	  Logical operators:
	  * `>=`, `<=`
	  * `=`, `!=`
	  * `AND`, `OR`, `IN`, `NOT`
	- ## `ORDER BY` Clause
	  ```SQL
	  ORDER BY <attrs> [ DESC | ASC ]
	  ```
	  Sorts the results by the comma-separated list of attributes, sorting in ascending order by default.
		- ### Example
		  ```SQL
		  SELECT S, STATUS
		  	FROM S
		      WHERE CITY = 'Paris'
		      ORDER BY STATUS DESC;
		  ```
	- ## `UNION` Clause
	  Merges two select statements akin to the union operator from [[Set Theory]].
	  
	  A statement getting all past and present senators:
	  ```SQL
	  SELECT FNAME FROM CurrentSenators
	  UNION
	  SELECT FNAME FROM PastSenators
	  ```
- ## Subqueries
  One option to ensure that the subquery returns *true*:
  ```SQL
  SELECT ...
  	...
      WHERE EXISTS
      	(SELECT ...)
  ```
  ...but what about where it returns *false*?
  
  One can simply convert `EXISTS` to `NOT EXISTS`:
  ```SQL
  SELECT ...
  	...
      WHERE NOT EXISTS
      	(SELECT ...)
  ```
- ## Group Functions
  * `SUM(<x>`
  * `AVG(<x>)`
  * `COUNT(<x>)`
  * `MAX(<x>)`
  * `MIN(<x>)`
  * `STDDEV(<x>)`
  * `VARIANCE(<x>)`
  ...all of which return a single value.