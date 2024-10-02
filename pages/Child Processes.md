### Important Calls
	- #### `fork`
	  Starts a child process with the same binary the parent started with
	- #### `wait`
	  Waits until *a* child process finishes
	- #### `exec`
	  Replaces current process image with a new process image
		- #### `execlp`
		  Takes a `nullptr`-terminated argument lists and tries to call the provided program, also checking the user's `$PATH`.
		- #### `execl`
		  The same as above, but does not check the user's `$PATH`.
		- #### `execp`
		  Takes only the program name and an array of arguments, also checking the `$PATH`.