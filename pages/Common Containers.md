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
	- ### Access
	  $$O(n)$$
	  In the worst case, it's $O(n)$ when it's the last element.
	- ### Deletion
	  $$O(n)$$
	  $O(n)$ otherwise at the worst case (it's the last element)
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