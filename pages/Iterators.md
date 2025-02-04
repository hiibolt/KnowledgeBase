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
	- #### `rbegin`
	  Returns the end of the iterator
	- #### `rend`
	  Returns the end of the iterator
	- #### `erase`
	  Removes the element specified by the iterator. Returns the next element.
	  ```cpp
	  std::vector<int> v = { 1, 2, 3, 4, 5 };
	  for ( auto it = v.begin(); v != v.end(); ) {
	  	if ( *it == 3 ) {
	        it = v.erase(it);
	      } else {
	        it++;
	      }
	  }
	  ```
- ## Types of Iterators
	- ### Input Iterators
	  Read-only, single-pass iterators for the purpose of reading elements from a container only once.
	  
	  Generally only has the `++` and `*` operators.
	- ### Output Iterator
	  Write-only, single-pass
	  
	  Generally only has the `++` and `*` operators.
	- ### Forward Iterator
	  Can only move forward, but supports both read and write
	- ### Bi-Directional Iterators
	  Can go both directions (such as `std::list`).
	- ### Random Access Iterators
	  Allows you to use `++`, `--`, and `[]`
	- ### Const Iterator (`const_iterator`)
	  Prevents the modification of elements