## Terms
	- ### Algorithm
	  A well-defined computational procedure that takes *inputs* and produces some value(s) as *output(s)*.
	- ### Loop Invariant
	  Help us understand why an algorithm is correct.
	  
	  Requires three properties to be satisfied:
	  * **Initialization**
	  It is correct prior to the first iteration of the loop
	  * **Maintenance**
	  If it is true before an iteration of the loop, it must remain true by the next iteration
	  * **Termination**
	  When the loop terminates, the invariant (and potentially, the reason for termination) provide useful information
- ## Sorting Algorithms
  Numbers that are to be sorted are often called *keys*.
	- ### Insertion Sort
	  * Rebuild the entire set from scratch
	  * Insert each key in its correct place one by one
	  ...this will result in a completely sorted array.
	  
	  For example, if you have $\vec{x}=\{1,3,4\}$ and need to insert everything from $\{2,3\}$, you would put $2$ at index 1 first, then put $3$ at index 3.
	- ### Merge Sort
	  Divide the array into two parts, and continue to do so until reaching the base case (the length of the array is zero). Finally, merge each array back up the chain.
- ## Common Approaches
	- ### Divide and Conquer
	  Splitting a problem into multiple smaller sub-problems, which are then solved up recursively and combined to create the solution to the original problem.