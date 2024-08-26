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
- ## Program Arguments
  Full `main` function prototype:
  ```cpp
  int main ( int argc, char* argv[] ) {
       ...
  }
  ```
  
  `argc` indicates the number of arguments.
  `argv` is an array of passed arguments. `argv[0]` is technically the first argument,