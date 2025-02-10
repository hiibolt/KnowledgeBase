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
  ```SQL
  UPDATE <table_name>
  	SET <attr> = <value> [, <attr> = <value> ...]
      [ WHERE <expression> ];
  ```
	- ### Example
	  ```SQL
	  UPDATE Student
	  	SET CLSYEAR = 'Senior'
	      WHERE TOTALHRS > 90;
	  ```
- ## Deletion
- ## Selection
- ## `WHERE` Clause
  Useful for specifying which rows to affect - commonly used with `UPDATE` and `SELECT` commands.