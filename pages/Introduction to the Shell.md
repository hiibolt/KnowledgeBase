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
  A **hard link** is a link that exists only in the context of a singular drive (with the exception of RAID). These are identified via the `inode`. They are replenishing, meaning if the linked-to is deleted, the linked-from will still exist.
  
  A **symbolic link** is a link that does *not* have an `inode`. Instead, it is a path to a file. Because of this, symbolic links can be made across various drives.
- With a symbolic link, you can create a (useful) cyclical link by linking `.` to `<link_name>`. 
  
  For example: