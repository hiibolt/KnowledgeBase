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
	  * `BASH` - The absolute path of the bash instance
	  * `RANDOM` - Returns a random number (0-32,767)
	  * `HOSTNAME` - Returns the name of the host
	  * `HOSTTYPE` - Platform type
	  * `PS1` - Changes the shell prompt
	  * `HISTSIZE` - Number of command lines to remember
	  * `?` - Return code (status) of last command
	  * `$` - Process ID (PID) of current shell
	- #### Event History
	  `$ history` - Outputs the history of the shell
	  
	  **Re-runs**:
	  * `$ !!` - By last command
	  * `$ 5` - By the event numebr
	  * `$ !-3`- By the number relative to
	  * `$ !ls` - By the text of the command used
- ## Syntax
	- ### Command Substitution
	  A command surrounded by backticks is substituted for Bash syntax. You can also use `$()`.
	  
	  Examples:
	  ```bash
	  echo `$PWD`
	  echo $($PWD)
	  ```
- ## Shell Scripting
	- #### Other Escape Characters
		- #### `\n`
		  Newline Character
		- #### `\t`
		  Tab Character
		- #### `\a`
		  Plays an alert sound
		- #### `\b`
		  Moves the cursor back one, allowing you to overwrite characters
	- ### Shebangs
	  A shebang specifies the binary for which the program should be interpreted by.
	  
	  For Python:
	  ```bash
	  #!/usr/bin/env python3
	  
	  print(":3")
	  ```
	  
	  For Bash:
	  ```bash
	  #!/bin/bash
	  
	  echo ':3' 
	  ```
	- ### Command Line Arguments
		- ### Positional Paramenters
		  Example:
		  ```bash
		  #!/bin/bash
		  echo $1
		  ```
	- ## Conditionals
	  * `1 || 2` - `2` is run only if `1` fails
	  * `1 && 2` - `2` is run only if `1` succeeds
		- #### Compound Logical Expressions
		  * `!` - Negates the output of the expression
		  * `-a` - True if both of the two expressions are true
		  * `-o`- True if one of the two expressions is true
		- ### Conditional Statements
			- #### If:
			  ```bash
			  if [ condition-1 ]; then
			  	statement-1
			  elif [ condition-2 ]; then
			      statement-2
			  else
			  	statement-3
			  fi
			  ```
			- #### Case
			  ```bash
			  case expression in
			  	match_1)
			      	statement_1
			          ;;
			      match_2)
			      	statement_2
			          ;;
			      *)
			      	default_statement
			          ;;
			  esac
			  ```
			- #### While
			  Executes while the condition is true
			  ```bash
			  while [ condition ]; do
			  	statement
			  done
			  ```
			- #### Until
			  Executes while the condition isn't true
			  ```
			  until [ condition ]; do
			  	statement
			  done 
			  ```
			- #### For
			  Executes a statement as many times as the number of words in the `word_list`
			  ```bash
			  for num in 1 2 3 4 5 6 7 8 9; do
			  	statement
			  done
			  ```
		- #### Relational Operators
		  *Note: Must use `test` to check whether an operator is true!*
			- #### Numeric
			  * `-gt` - Greater than
			  * `-ge` - Greater than or equal to
			  * `-lt` - Less than
			  * `-le` - Less than or equal to
			  * `-eq` - Equal to
			  * `-ne` - Not equal to
			- #### String
			  * `=` - Equal to
			  * `!=` - Not equal to
			  * `-z str` - String length is zero
			  * `-n str` - String length is non-zero
			  * `file1 -nt file2` - `file1` is newer than `file2`
			  * `file1 -ot file2` - `file1` is older than `file2`