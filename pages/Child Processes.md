### Important Calls
	- #### `fork`
	  Starts a child process with the same binary the parent started with
	- #### `wait`
	  Waits until *a* child process finishes
	- #### `exec`
	  Replaces current process image with a new process image
		- #### `execlp`
		  Takes a `nullptr`-terminated list of arguments and tries to call the provided program,