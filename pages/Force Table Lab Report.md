public:: true

- ### Metadata
  Date: *September 29, 2022*
  Class: *PHYS253 - Section 1*
  Author: *John White*
  Professor: *Jarod Adelman*
- # Theory
	- ## Primary Objectives
	  In this lab, we will...
	  * Calculate the **x** and **y** components of vectors
	  * Compute the equal and opposite force to a pair of vectors
	  * Calculate the error percentages between a calculated and measured value
- # Data
	- ## 2.1 Vector X and Y components
		- ## Section 1
		  **Forces**
		  1.96N @ 60deg and 1.96N @ 300deg
		  
		  **Measured Balancing Weight**
		  150g @ 180deg
		- ## Section 2
		  **Forces**
		  2.45N @ 30deg and 2.45N @ 120deg
		  
		  **Measured Balancing Weight**
		  282g @ 255deg
		- ## Section 3
		  **Forces**
		  1.47N @ 30deg and 1.96N @ 270deg
		  
		  **Measured Balancing Weight**
		  132g @ 136deg
- # Results
	- ## 3.1 Equilibrium Weight
	  First, I created a Desmos calculator to calculate the components of the final vector. **a** and **b** are the **x** and **y** components respectively of the first weight, and **c** and **d** are the **x** and **y** components of the second weight.
	  
	  **First two equations:**
	  These calculate the actual weight of each hook-weight system.
	  
	  **Equations 3-6:**
	  These calculate the **x** and **y** components of each system.
	  
	  **Equations 7-8:**
	  These two calculate the **x** and **y** components of the vector (the flip effect is not calculated, I do it manually to ensure my results are relevant.)
	  
	  **Equations 9-10:**
	  The first calculates the magnitude (N).
	  The second calculates the angle (deg), but 180 still needs to be added.
	  
	  ![image.png](../assets/image_1696277462627_0.png)
		- ### Section 1:
		  ![image.png](../assets/image_1696298957854_0.png)
		- ### Section 2:
		  ![image.png](../assets/image_1696299002530_0.png)
		- ### Section 3:
		  ![image.png](../assets/image_1696299027545_0.png)
	- ## Percent Error
	  I calculated each percent error with the following formula:
	  $$\frac{true - measured}{true}*100\% \text{ = Percent Error.} $$
- # Discussion
  I was first tasked with calculating the **x** and **y** components of each weight. I did this by first adding the mass of the weight and hanger together, converting to **kg**, and converting to Newtons.
  
  Next, I multiply by the cosine and sine of the angle of the weight (relative to the +x axis) to get the **x** and **y** components.
  
  Following this, I am tasked with finding the components of the equivalence vector. I do this by simply adding the **x** and **y** components, then taking the square root of both squared added to get the magnitude. I find the angle by taking $$arctan(\frac{y}{x})$$ and adding 180.
  
  Finally, I calculate the percent error using the above formula.
  
  
  In my case, I created a calculator to streamline my work. I believe that the masses were not accurate, which contributed to the errors.
- # Conclusion
  This was a very fun lab. I enjoyed being able to physically see equations in motion, even if there was some error.
  
  The only thing I would change would be to provide an explanation for said error in the final result, whether it be an excerpt in the manual or a full section dedicated to the concept.