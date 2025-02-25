## Problems to Which DP Applies
**Use DP When**:
* Polynomial number of sub-problems
* The final solution can be made up of the sub-problems
* There is a natural ordering of "small" to "large" problems
* A sub-problem can be computed from even smaller sub-problems
- ## Top-Down vs Bottom-Up
	- ### Top-Down + Memoization
	  Starting with the highest problem, and recursing down until you reach the smallest possible sub-problems.
	  
	  This is akin to doing it the "natural" way.
	- ### Bottom-Up (Tabulation)
	  Solve it in size order, from the bottom, and save the solution. As we move to higher sub-problems towards the main problem, we already have the work for the smaller sub-problems saved.
	  
	  Generally faster, iterative, and doesn't cause stack overflow.