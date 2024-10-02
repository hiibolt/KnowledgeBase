### Important Calls
	- #### `fork`
	  Starts a child process with the same binary the parent started with
	- #### `wait`
	  Waits until *a* child process finishes
	- #### `exec` Family
	  Replaces current process image with a new process image
		- #### `execl`
		  Takes a `nullptr`-terminated argument lists and tries to call the provided program.
		- #### `execlp`
		  Takes a `nullptr`-terminated argument lists and tries to call the provided program, also checking the user's `$PATH`.
		- #### `execv`
		  Takes only the program name and an array of arguments.
		- #### `execvp`
		  Takes only the program name and an array of arguments, checking the `$PATH`.
	- #### `pipe`
	  Creates a pipe which chains two file descriptors.
- ### Spawning Additional Processes
  It's not possible to spawn an additional process with only one system call.
  
  Instead, you must:
  * Fork into a child process
  * Morph the child process into the desired one