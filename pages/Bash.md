#### Customization
* `~/.bash_profile` is login session shell
* `~/.bashrc` if invoked from command line
- ### Variables
  * Always stored as strings or arrays of strings
  * Strings with quotes should have quotes around them
	- #### Setting a variable:
	  `$ <variable>=<string_value>`
	- #### Retrieving a variable
	  `$ echo $<variable>`
	- #### Predefined Variables
	  * `HOME` - The path to the user's home directory
	  * `PATH` - List of directories to search for commands
	  * `MAIL` - Absolute path to your system mailbox
	  * `USER` - Your username
	  * `SHELL` - Absolute path to your *login shell*
	  * `TERM` - Format of terminal being used
	  * `PWD` - Current working directory
	  * `EDITOR` - Default editor to use when needed
	  * `DISPLAY` - Where GUI apps should show (X server)
	  * `BASH` - The absolute path of the **bash** instance
	  * `RANDOM` - Returns a random number
	  * `HOSTNAME` - Returns the name of the host
	  * `HOSTTYPE` - Platform type
	  * `?` - Return code (status) of last command
	  * `$` - Process ID (PID) of current shell