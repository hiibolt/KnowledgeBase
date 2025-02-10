## Insertion
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
- ## Updating
- ## Deletion
- ## Selection