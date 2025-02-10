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
  DELETE FROM <table_name> [ WHERE <expression> ]
  ```
	- ### Example
	  Deletes every `Person`
	  ```SQL
	  DELETE FROM Person
	  ```
	-
- ## Selection
- ## `WHERE` Clause
  Useful for specifying which rows to affect - commonly used with `UPDATE` and `SELECT` commands.