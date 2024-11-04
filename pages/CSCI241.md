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