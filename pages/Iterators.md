## Definition
Used to help define universal traversal for advanced data structures - particularly useful for non-contiguous ones.

There are also some data structures that cannot be iterated over without modifying it, such as a `stack` or `queue` *adapter container* (a container that does not have its own container).
- ### Common Methods
	- #### `begin`
	  Returns an instance of `Iterator` that points to the start of the data structure
	- #### `end`
	  Returns an instance of `Iterator` that points to the end of the data structure
	- #### `operator<*>`
	  Allows you to deference an `Iterator` into the underlying element that it currently points to.