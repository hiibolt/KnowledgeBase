public:: true

- ### Metadata
  Date: *November 5th, 2023*
  Class: *PHYS253 - Section 1*
  Author: *John White*
  Professor: *Jarod Adelman*
- # Theory
	- ## Primary Objectives
	  In this lab, we will...
	  * -
	  * -
	  * -
- # Data
	- ## 2.1 Experimental Procedure
	  | Trial | Bob Mass (g)| Hanging Mass (g) | D (cm) | d (cm) | r (cm) | n | Time Difference (s) |
	  |1|429.0|576.7|6|11|14|50|33.25|
	  |2|429.0|666.4|6|12|15|50|29.83|
	  |3|429.0|849.5|6|13|16|50|29.01|
	  |4|429.0|929.6|6|14|17|50|28.18|
	  |5|429.0|1047.1|6|15|18|50|27.17|
- # Results
	- ## 3.1 - Calculating Forces
	  I calculated the following results using Python, which I will further discuss in ((9bce9233-62d1-47bb-abea-6ec62c741849)).
		- ### Trial 1
		  F_spring: 5.65166 
		  F_centripital: 5.361691
		- ### Trial 2
		  F_spring: 6.53072 
		  F_centripital: 7.137429
		- ### Trial 3
		  F_spring: 8.3251 
		  F_centripital: 8.049735
		- ### Trial 4
		  F_spring: 9.11008 
		  F_centripital: 9.064085
		- ### Trial 5
		  F_spring: 10.26158 
		  F_centripital: 10.324054
	- ## 3.2 Percent Differences:
	  I also calculated the percent error for each trial with Python:
		- ### Trial 1
		  Percent Difference: 5.26577415936465%
		- ### Trial 2
		  Percent Difference: 8.877702812485234%
		- ### Trial 3
		  Percent Difference: 3.3632753321102915%
		- ### Trial 4
		  Percent Difference: 0.5061553237945114%
		- ### Trial 5
		  Percent Difference: 0.60696660302124%
- # Discussion
  id:: 9bce9233-62d1-47bb-abea-6ec62c741849
	- ## 4.1 Calculating Forces
	  I was tasked to calculate both the spring force and the centripetal force. I derived the following equations for both respectively:
	  $$F_s = Mg$$
	  $$F_c = m\frac{4{\pi}^2n^2}{t^2}r$$
	  
	  However, this is not Python code, so here are the following equations in Python form:
	  ```python
	  F_spring = trial["hanging_mass"] / 1000 * 9.8
	  ```
	  ```python
	  F_centripital = (bob_mass / 1000 * 4 * (math.pi ** 2) * (n ** 2) * trial["r"] / 100 ) 
	      / (trial["time_difference"] ** 2)
	  ```
	  It's worth noting that the **/ 100**s and **/ 1000**s you see are unit conversion between cm/m and g/kg respectively.
	- ## 4.2 Percent Difference
	  Next, I was tasked with calculating the percent difference between the two forces for each trial.
	  
	  The following formula is considered standard for percent difference:
	  
	  $$\%\text{ Difference} = \frac{|F_c-F_s|}{\frac{1}{2}(F_c+F_s)}$$
	  
	  I do this in the following way with python for each trial and their respective forces:
	  
	  ```python
	  percent_difference = (F_centripital - F_spring) / ((F_spring + F_centripital ) / 2) * 100
	  ```
	- ## 4.3 Analytics
	  I decided to print these with Python for easier human reading with the following code:
	  ```python
	  print(f"Trial {trial['trial']}
	     \nF_spring: {round(F_spring, 6)}
	     \nF_centripital: {round(F_centripital, 6)}
	     \nPercent Difference: {percent_difference}\n")
	  ```
	- ## 4.F Final Code
	  ```python
	  bob_mass = 429.0
	  D = 6
	  n = 50
	  
	  data = [
	  	{
	      "trial": 1,
	      "hanging_mass": 576.7,
	      "d": 11,
	      "r": 14,
	      "time_difference": 33.25
	  	}, 
	  	{
	  		"trial": 2,
	  		"hanging_mass": 666.4,
	  		"d": 12,
	  		"r": 15,
	  		"time_difference": 29.83
	  	}, 
	  	{
	  		"trial": 3,
	  		"hanging_mass": 849.5,
	  		"d": 13,
	  		"r": 16,
	  		"time_difference": 29.01
	  	}, 
	  	{
	  		"trial": 4,
	  		"hanging_mass": 929.6,
	  		"d": 14,
	  		"r": 17,
	  		"time_difference": 28.18
	  	}, 
	  	{
	  		"trial": 5,
	  		"hanging_mass": 1047.1,
	  		"d": 15,
	  		"r": 18,
	  		"time_difference": 27.17
	  	}
	  ]
	  
	  for trial in data:
	  	F_spring = trial["hanging_mass"] / 1000 * 9.8
	  	F_centripital = (bob_mass / 1000 * 4 * (math.pi ** 2) * (n ** 2) * trial["r"] / 100 ) / (trial["time_difference"] ** 2)
	  	percent_difference = (F_centripital - F_spring) / ((F_spring + F_centripital ) / 2) * 100
	  
	  	print(f"Trial {trial['trial']}\nF_spring: {round(F_spring, 6)} \nF_centripital: {round(F_centripital, 6)}\nPercent Difference: {percent_difference}\n")
	  ```
- # Conclusion
  This lab was