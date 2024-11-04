## Usage
* Inline Script `sed -e "address command" file`
* Script file `sed -f script.sed file`
	- ### Common Options
	  * `-i` - Allows the input file to be changed
	  * `-n` - Line is no longer sent to output
	  * `-e` - Takes from an expression as the `sed` script
	  * `-f` - Takes contents of a file as the `sed` script
	- ### Address Types
	  **Basic Types**:
	  * `sed -n -e '3 p' file` - Line 3
	  * `sed -n -e '$ p' file` - Last line
	  * `sed -e '10 s/endif/fi/` - Substitute `endif` with `fi` on line 10
	  These are generally useful for quick substitutions.
	  
	  **Range Types**:
	  * `<start>,<end>` - From line \#`start` to line \#`end`
	  * `<start>,/RE/` - From line \#`start` to `/RE/`
	  These are generally very useful for selecting variadic ranges.
	  
	  **Nested Addresses**:
	   ```sed
	  - 20,30{
	  - /^$/ p
	  - }
	  ```
	  ...which prints all empty lines.
	  
	  Note that you can use the `!` operator to negate the current address:
	  * `sed -n -e '3 ! p' file` - Prints nothing except line 3
	- ### Common Operations
	  * `d` - Deletes
	  * `p` - Prints
	  * `s` - Substitutes 
	  ```bash
	  sed -e '1 s/meow/meowww/g' file
	  ```
	  ...which would replace occurrences on line 1 of "meow" with "meowww".
	  
	  Using an `&` in the replacement field (second section of the triple forward slashes) will be substituted for the entire match. Useful for append and delete with more granular control.
	  
	  Using a backslash and number (`\<n>`) in the replacement field will be substituted for a specific match group number, which is useful for being more specific with which you'd like.
	  * `=` - Prints the current line number
	  * `i` - Inserts line(s) before the address
	  * `a` - Appends line(s) after the address
	  * `c` - Replaces the whole line with new text
	  * `n`- Skips to the next line
	  * `N` - Also process the next line
	  * `r` - Reads from a file
	  * `w` - Writes to a file