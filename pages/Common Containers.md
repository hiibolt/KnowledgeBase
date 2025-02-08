## Static Arrays
An array with a size known at compile time. Extremely efficient.
	- ### Access
	  id:: 67a50209-ede4-4299-9bf0-f52c621b38ff
	  $$O(1)$$
	  Very fast, as the compiler knows exactly where to look.
	- ### Search
	  id:: 67a503d0-b1b7-4342-8ee6-cf727dfb6e15
	  $$O(n)$$
	  $O(n)$ in the worst case where it's the last element.
	- ### Insertion
	  $$O(1)\text{ or }O(n)$$
	  $O(1)$ if at the end, $O(n)$ if you must shift elements
	- ### Deletion
	  $$O(1)\text{ or }O(n)$$
	  $O(1)$ if at the end, $O(n)$ if shifts are required.
- ## Dynamic Arrays
  A dynamic array can be created with a variable size, and the size does not need to be known at compile time.
  
  {{embed ((67a50209-ede4-4299-9bf0-f52c621b38ff))}}
  {{embed ((67a503d0-b1b7-4342-8ee6-cf727dfb6e15))}}
	- ### Insertion
	  $$O(1)\text{ or }O(n)$$
	  $O(1)$ if at the end and $O(n)$ if shifts are required or the dynamic arrray must be extended.
	- ### Deletion
	  $$O(1)\text{ or }O(n)$$
	  $O(1)$ if at the end and $O(n)$ if shifts are required or the dynamic array shrinks.
	- ### Resizing
	  $$O(n)$$
	  $O(n)$ as each element must be copied into the new chunk of memory.
- ## Singly Linked List
  id:: 67a50613-434c-4717-8ba9-9c831d8baa79
	- ### Insertion
	  id:: 67a69ecd-40e3-40e9-b547-a56f407db31d
	  $$O(1)\text{ or }O(n)$$
	  $O(1)$ in the scenario that you're inserting at the start, $O(n)$ at the worst case (last element).
	- ### Access
	  id:: 67a50678-c8e5-4415-8a9c-235c1cc0d883
	  $$O(n)$$
	  In the worst case, it's $O(n)$ when it's the last element.
	- ### Deletion
	  id:: 67a50791-4588-4b18-85b0-2b513af3741e
	  $$O(n)$$
	  $O(n)$ otherwise at the worst case (it's the last element)
- ## Doubly Linked List
  The same as a ((67a50613-434c-4717-8ba9-9c831d8baa79)), but also adds some overhead in the form of a *prev* pointer to the prior element.
  
  Generally speaking, the same complexity, but for operations involving the last element, drops complexity. For example, ((67a69ecd-40e3-40e9-b547-a56f407db31d)), ((67a50791-4588-4b18-85b0-2b513af3741e)), and ((67a50678-c8e5-4415-8a9c-235c1cc0d883)) can drop to $O(1)$.
	- ### C++ Implementation
	  Can be found as the `std::list` container.
	- ### Rust Implementation
	  The `std::collections::LinkedList` type. ([Link](https://doc.rust-lang.org/std/collections/linked_list/struct.LinkedList.html))
- ## Stack
  A LIFO (last in, first out) data structure.
	- ### Push
	  $$O(1)$$
	  Added to the end every time.
	- ### Pop
	  $$O(1)$$
	  Removed from the end every time
	- ### Peek / Top
	  $$O(1)$$
	  Always looks at the element on the end.
- ## Queue
  A FIFO (first in, first out) data structure.
	- ### Push
	  $$O(1)$$
	  Added to the end every time.
	- ### Pop
	  $$O(1)$$
	  Removes from the start every time.
	- ### Peek / Top
	  $$O(1)$$
	  Looks at the start every time.