### Versus "sed"
* Perform arithmetic and string operations
* Use conditionals and loops
* Splits lines into "fields"
- ## Basic Usage
  * `awk 'script' file`
  * `awk -f scriptfile file`
  ...which are the text-input / scripfile usages.
  
  **Example Text Input Usage**:
  ```bash
  $ cat emps
  Tom Jones      4424    5/12/66   543354
  Mary Adams     5346    11/4/63   28765
  
  $ awk '/Tom/ { print }' emps
  Tom Jones      4424    5/12/66   543354
  
  $ awk '{print NR, $0}' emps
  1 Tom Jones      4424    5/12/66   543354
  2 Mary Adams     5346    11/4/63   28765
  
  
  $ cat emps2
  Tom Jones:4424:5/12/66:543354
  Mary Adams:5346:11/4/63:28765
  
  $ awk -F: '/Jones/{print $1, $2}' emps2
  Tom Jones 4424
  ```
  ...but for longer or more complex scripts use the below.
  
  **Example Script Usage**:
  ```
  BEGIN {
  	print "Mon Sales Revenue"
      count=0
  }
  /[0-9]+/ {
  	print $1, $2+$3+$4, $5
      count++
  }
  END {
  	print count, " records processed"
  }
  ```
  ...but how does one change their field separator, or another system variable?
  
  **Using System Variables in Scripting**:
  ```
  BEGIN {
  	FS=":"
      count=0
      print "list of users that use bash"
  }
  /bash/ {
  	print $1, $5
      count++
  }
  END {
  	print count, " users use bash"
  }
  ```
	- #### Options
	  * `-F<sep>` - Changes field separator
	  * `-f file` - Use scriptfile
	- ### Variables
		- #### Local
		  ```bash
		  $ awk '$1 ~ /Tom/
		       {wage = $3 * $4; print wage}'
		       file
		  ```
		  
		  ```bash
		  $ cat grades
		  john 85 92 78 94 88
		  
		  $ cat script
		  { 
		      total = $2 + $3 + $4 + $5 + $6;
		      average = total / 5;
		      print average
		  }
		  
		  $ awk -f script
		  ...
		  ```
		- #### System
		  * `NR` - Number of the current record
		  * `NF` - Number of fields in current record
		  * `FS` - Field separator (with the default being whitespace)
		  * `$0` - Entire line
		  * `$<n>` - `<n>`th
		  * `BEGIN` - Matches before the first line (useful for headers)
		  * `END` - Matches after the last line of input (useful for footers)
	- ### Conditional REGEX Matching
	  * `awk '$5 ~ /E/ {print $1, $2}` - Print columns 1 and 2 given column 5 *is* `E`
	  * `awk '$5 !~ /E/ {print $1, $2}` - Print columns 1 and 2 given column 5 *is not* `E`
	- ### Arithmetic, Conditional, and Logical Operators
	  All basic mathematical, conditional, and logical operators are available.
	  
	  **Example**:
	  * `$ awk '$3 * $4 > 500 {print}' file` - Prints the line if column 3 times column 4 is over 500
	- ### Conditional Range Patterns
	  **Example**:
	  `awk '/blue/,/yellow/ print' file` - Prints ranges inclusively, also considering SOF and EOF
	- ### Actions
	  `awk` has many actions other languages have, such as:
	  * `print`, `printf`, `sprintf`
	  * `while`, `for`, `loop`
	- ### Print Formatting
	  * `$ awk '{print $1, $2}' grades` - Would print `john 98`
	  * `$ awk '{print $1 "," $2}' grades` - Would print `john,98`
	  * `$ awk '{OFS="-"; print $1, $2}' grades` - Would print `john-98`
	  * `$ awk '{OFS="-"; print $1 "," $2}' grades` - Would print `john,98`
	  ...but, you can also use more specific specifiers with `printf` or `sprintf`:
	  
	  **Format Specifiers**:
	  * `%d, %i` - Decimal int
	  * `%c` - Character
	  * `%s` - String
	  * `%f` - Float
	  * `%o` - Octal
	  * `%x` - Hex
	  * `%e` - Scientifically notated float
	  * `%%` - The character %
	  ...but what does the syntax actually look like?
	  
	  **Example**:
	  ```
	  printf("The character is %c\n", x)
	  
	  result = sprintf("The character is %c\n", x)
	  print(result)
	  ```
	- ### Piping and Redirection
	  ```
	  $ awk '{print $1,$2 | "sort"}' grades
	  andrea 89
	  jasper 84
	  john 85
	  ```
	  ...and to output:
	  
	  ```bash
	  $ awk '{print $1 , $2 > "file"}' grades
	  $ ls
	  file grades
	  $ cat grades
	  jasper 84
	  john 85
	  andrea 89
	  ```
	- ### Builtins
	  * `tolower(string)` - Returns lowercase copy of input
	  * `toupper(string)` - Returns uppercase copy of input
	- ### Arrays
	  Array elements default to `0` or an empty string.