## Terminology
	- ### `stdin`
	  Standard input stream
	- ### `stdout`
	  Standard output stream
	- ### `stderr`
	  Standard error stream
	- ### Dotfile
	  Directories or files prefaced with a period (`.file`).
- ## Simple Commands
	- ### `ls`
	  Lists the contents of the current directory
	  
	  Arguments:
	  * `-a` - Lists all contents
	  * `-l` - Adds additional information to each entry
	- ### `pwd`
	  Prints the path of the current working directory
	- ### `clear`
	  Clears the shell screen
	- ### `date`
	  Prints the current date and time
	- ### `passwd`
	  Allows you to change your password
	- ### `exit`
	  Closes the current SSH session (also applies to other contexts)
	- ### `sort`
	  Sorts the provided arguments in alphabetical order.
	  
	  Arguments:
	  * `-r` - Reverses the order of output.
	- ### `more`
	  Shows the content of a file, page by page
	- ### `logout`
	  Logs you out of the shell
	- ### `who`
	  Shows currently logged in users
	- ### `script`
	  Makes a record of a terminal session
	- ### `uname`
	  Prints the current OS information
	- ### `man`
	  Prints the manual for a command, if it exists
- ## Program Arguments
	- #### Full `main` function prototype:
	  ```cpp
	  int main ( int argc, char* argv[] ) {
	       ...
	  }
	  ```
	- #### Arguments
	  * `argc` indicates the number of arguments.
	  * `argv` is an array of the passed arguments.
	  * `argv[0]` is technically the first argument - the command name.