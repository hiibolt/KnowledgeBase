## Review for Exam 1
* **Bubble (Sinking)**: Every pass, each pair of two numbers, and swap the larger to be the second
* **Selection**: Every pass, place the smallest element at the start of the array
* **Insertion**: (First Pass): Create an array with the first element. For each next pass, pick the next element, and place it into the array in its correct position. At the end, you will have a completely sorted array.
* **Quick Sort (Partition Type 1)**: Pick a pivot value (middle value). Come from the left until you find a value larger than the pivot. Then, come from the right, and pick a value less than the pivot. Swap them. When the two searches intersect, pick the smaller of the two intersects, and swap it with the pivot value. Then, call the quick sort recursively on the arrays left and right of the old pivot value.
* **Quick Sort (Partition Type 2)**: Pick a pivot value (middle value), and swap it to index 0. Start from the left, and find the first value less than the pivot. When you find one, swap it to the first available spot that hasn't yet been swapped to. At the end, swap the last swapped index into index 0 to be our new pivot value.
- ## Review for Exam 2
  * Formatting for unary and binary operators
  Unary member functions have no arguments, whereas non-member functions have one
  Binary operators as members have one argument, whereas non-member functions have two
  
  Non-overloadable operators:
  * `.`
  * `.*`
  * `::`
  * `?:`
  * `sizeof( item )`
  ...reason varies, but usually, you don't need to overload these anyways.
  
  Operators which MUST be members of the class:
  * `=`
  * `[]` (needs a reference and mutable reference)
  ...this is because these need to be able to directly modify the class?
  
  Operators which require more than one implementation:
  * `[]`
  * `++` and `--` (they have pre and postfix versions)
  ...you can't only write one, sadly. Index needs a const and non-const reference return type.
  
  If the `rhs` of an operator is left unmodified, be sure to specify `const`. Similarly, if the host class is left untouched, add `const` to the end of the function signature just before the semicolon.
  
  Operators which aren't members of a class must be `friend` functions in order to access otherwise private data members.
  
  It's worth noting that the `delete` operator works slightly different for an array:
  ```cpp
  delete [] some_pointer
  ```
  ...that being that it requires the `[]` you see above.
  
  For the assignment operator, it must always return a reference to the class object. For example:
  ```cpp
  O & operator= ( const O & rhs );
  ```
  ...noting that reference at the beginning.
  
  In general, there are 5 basic steps for overloading the assignment operator:
  * 1.) Check for self-assignment (cloning self)
  ```cpp
  if ( this != &rhs ) {
  	return *this;
  }
  ```
  * 2.) Free up memory (`delete`)
  * 3.) Get new memory (`new`)
  * 4.) Copy the information to memory
  * 5.) Return the object itself (`return *this`)
  ...this is likely on the exam. No way she'd go this in-depth otherwise, right?
  
  **Linked Lists**:
  Know how to:
  * Insert a node into a given list
  * Delete a node into a given list
  * Search a given list
  * Print a given list (iteratively or recursively)
  * Count the number of nodes in a given list (iteratively or recursively)
  ...it's worth practicing this on LC or locally.
  
  **Stacks**:
  Know how to:
  * Use both FIFO or LIFO
  * Understand overflow (too many items) and underflow (no items to pop)
  * Implement an item addition algorithm
  * Implement an item removal algorithm