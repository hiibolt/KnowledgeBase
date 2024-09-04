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
	  * `-t` - Sorts by timestamp
	  * `-s` - Sorts by size
	  * `-r` - Reverses the current sort order
	- ### `pwd`
	  Prints the path of the current working directory
	- ### `clear`
	  Clears the shell screen
	- ### `date`
	  Prints the current date and time
	  
	  Arguments:
	  * `+%F` - Prints in **YYYY-MM-DD** (useful for chronological sorting)
	- ### `passwd`
	  Allows you to change your password
	- ### `exit`
	  Closes the current SSH session (also applies to other contexts)
	- ### `sort`
	  Sorts the provided arguments in alphabetical order
	  
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
	  
	  Arguments:
	  * `-s` - Specifies the section to search for the manual in
	- **`ln`**
	  Creates a hard link that allows a file or directory to be reference by another name.
	  
	  To create a symbolic link, use the `-s` option.
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
- ## Link Types
  id:: 66d1fa78-88f6-4aaa-a9db-7c0818b523d3
  A **hard link** is a link that exists only in the context of a singular drive (with the exception of RAID). These are identified via the `inode`. They are replenishing, meaning if the linked-to is deleted, the linked-from will still exist.
  
  A **symbolic link** is a link that does *not* have an `inode`. Instead, it is a path to a file. Because of this, symbolic links can be made across various drives.
	- ### Cyclical Link
	  With a symbolic link, you can create a (useful) cyclical link by linking `.` to `<link_name>`. 
	  
	  For example:
	  ```bash
	  ln -s . f
	  ```
- ## Types of Files
	- ### Regular Files
	  Text, binary, or executable files stored as a collection of bytes.
	- ### System Files
	  Specialized files for devices, networking endpoints, etc
	- ### Directories
	  Contains other ifels
	- ### Links
	  ((66d1fa78-88f6-4aaa-a9db-7c0818b523d3))
- ### Wildcard and Question Select
	- ### `*`
	  Allows a match for *any* zero or more characters at this position
	- ### `?`
	  Matches any single character at this position
	- ### `[]`
	  Allows any of a list (inside the `[]`) of possible characters at this position.
	  
	  Use `^` to invert.
	- ### `{}`
	  Allows any of a list (inside the `{}`, separated by `,`) of possible characters at this position.
	  
	  Use `^` to invert.