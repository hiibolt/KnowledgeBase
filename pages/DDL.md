## Tables
	- ### Creating a table
	  ```SQL
	  CREATE TABLE <table_name> {
	  	<attribute> <type> [NOT NULL] [UNIQUE] [PRIMARY KEY], [ ... ]
	      [PRIMARY KEY(<pkattrs>),]
	      [FOREIGN KEY(<attrs_here>) REFERENCES <home_table>(<attrs_in_home>)]
	  };
	  ```
	  ...where:
	  * `pkattrs` is a comma-separated list of the attributes composing the primary key
	  * `attrs_here` is a comma-separated list of the attributes composing the foreign key
	  * `attrs_here` matches a set of attributes in the home table `attrs_in_home`
	  
	  **Naming**:
	  * Valid characters: `A-Za-z`, `$`, `_`, `0-9` (after the first letter)
	  * All names must be unique
	  * Max length of 64 characters
		- #### Example
		  **Person**($$\underline{\text{SSN}}$$, FNAME, LNAME, PHONE)
		  ```SQL
		  CREATE TABLE Person(
		  	SSN   CHAR(9) PRIMARY KEY, # Social security number
		    	FNAME CHAR(20) NOT NULL,   # First name
		    	LNAME CHAR(20) NOT NULL,   # Last name
		    	PHONE CHAR(10)             # Phone #
		  );
		  ```
	- ### ALTER TABLE
	- ### DROP TABLE
- ## Views
	- ### CREATE VIEW
	- ### DROP VIEW
- ## Datatypes
  * `INT/INTEGER`
  * `FLOAT`
  * `DOUBLE/REAL`
  * `DECIMAL` - A decimal with `i` total digits, `j` digits after the decimal point
  * `CHAR(n)` - A character string exactly `n` characters long
  * `VARCHAR(n)` - A variable length string with at most `n` characters in length
  * `DATE` - A date in the form `YYYY-MM-DD`
  * `TIME` - A time in the form `HH:MM:SS`
  * `DATETIME` - `YYYY-MM-DD HH:MM:SS`
  * `TIMESTAMP` - The same as `DATETIME`, but in UTC
- ## Column Options
  * `NULL` - Allows `NULL` as a value (default)
  * `NOT NULL` - Disallows `NULL` as a value
  * `UNIQUE` - No two tuples can have the same value
  * `PRIMARY KEY` - Declares this sole attribute as the *entire* primary key (for multiple, use the `PRIMARY KEY (<a>, <b>, <c>, ...)`)
  * `AUTO_INCREMENT` - Increments previous value if nothing is provided
  * `DEFAULT <x>` - Sets the default value to `x`
- ## Comments and Quotes
  Use `#` for `--` EOL comments.
  Use `/**/` for multi-line comments
  
  Use " ' " for values and " ` " for identifiers.