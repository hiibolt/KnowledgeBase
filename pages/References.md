- # De-Referencing Operator **\***
  Takes a pointer and transforms it into the underlying value
	- ## De-ref Coercion
	  id:: 64bae2cf-9355-4d13-b07e-b8395181c451
	  Accessing a field of a pointer to an object as follows
	  ```rust
	  struct Something {
	  	value: i16
	  }
	  
	  let something: Something          = Something { value: 8 };
	  let something_pointer: &Something = &something;
	  something_pointer.value \= 2;
	  
	  println!("{}", something);
	  >>>>Output: 4
	  ```
	  expands something_pointer.value to (*something_pointer).value automatically.