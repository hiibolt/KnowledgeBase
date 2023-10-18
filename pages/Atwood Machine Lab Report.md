public:: true

- ### Metadata
  Date: *October 10, 2023*
  Class: *PHYS253 - Section 1*
  Author: *John White*
  Professor: *Jarod Adelman*
- # Theory
	- ## Primary Objectives
	  In this lab, we will...
	  * Measure the relationship between mass difference between a two-weight pulley system
	  * Calculate little G by the trendline of the relationship between weight difference and time
	  * Calculate the error percentages between a calculated and measured value
- # Data
	- ## 2.1
	  Weight 1: 118.2
	  Weight 2: 119.1g
	  Pulley: 465g
	  Distance between photogates: 64.5cm
	  
	  | Weight - Mass 1 (g) | Weight - Mass 2 (g) | Time (s) |
	  | 50 | 75 | 1.448311 |
	  | 45 | 80 | 1.264709 |
	  | 40 | 85 | 1.0909185 |
	  | 35 | 90 | 1.039192 |
	  | 30 | 95 | 0.9988435 |
	  | 25 | 100 | 0.9724234 |
	  | 20 | 105 | 0.936344 |
	  | 15 | 110 | 0.908686 |
	- ...
- # Results
	- # Preface
	  I decided to format my data as follows in a ``data`` variable:
	  ![image.png](../assets/image_1697658510310_0.png)
	- ## 3.1 Calculating Acceleration
	  I achieve this by first adding the mass of the weights themselves and converting to kilograms. Next, I populate the ``weight_difference`` field, and finally I calculate and populate the ``acceleration`` field with the equation $$a = \frac{m_2 - m_1}{m_2 + m_1 + \frac{m_p}{2}}g$$
	  ![image.png](../assets/image_1697658492894_0.png)
	- ## 3.2 Graphing the data
	  I then plot the data. I extract the data from each point into a list using a shorthand tactic called *list comprehension*.
	  ![image.png](../assets/image_1697658613875_0.png)
	  My graph looks the following way:
	  ![image.png](../assets/image_1697658748396_0.png)
	- ## 3.3 Collecting the Slope and Calculating Little G
	  I do this by grabbing the coefficient of the slope ($$m$$) and reversing the equation $$a = \frac{m_2 - m_1}{m_2 + m_1 + \frac{m_p}{2}}g$$ to solve for $$g$$.
	  
	  The following code does so, as well as calculating the percent error between real little g: ![image.png](../assets/image_1697658929517_0.png)
- # Discussion
  ...
- # Conclusion
  ...