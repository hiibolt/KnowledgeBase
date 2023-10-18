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
	  
	  And finally, I get the following results: 
	  ![image.png](../assets/image_1697658945438_0.png)
	- ## Complete Code
	  ```python
	  import matplotlib.pyplot as plt
	  import numpy as np
	  from math import sin, cos, radians
	  from sklearn.metrics import r2_score
	  
	  
	  data = [
	  	{
	  		"m1": 50,
	  		"m2": 75,
	  		"time": 1.448311,
	  		"weight_difference": None,
	  		"acceleration": None
	  	},
	  	{
	    	"m1": 45,
	  		"m2": 80,
	  		"time": 1.264709,
	  		"weight_difference": None,
	  		"acceleration": None
	   	},
	  	{
	  		"m1": 40, 
	  		"m2": 85,
	  		"time": 1.090918,
	  		"weight_difference": None,
	  		"acceleration": None
	  	},
	  	{
	  		"m1": 35,
	  		"m2": 90,
	  		"time": 1.039192,
	  		"weight_difference": None,
	  		"acceleration": None
	  	},
	  	{
	  		"m1": 30,
	  		"m2": 95,
	  		"time": 0.9988435,
	  		"weight_difference": None,
	  		"acceleration": None
	  	},
	  	{
	  		"m1": 25,
	  		"m2": 100,
	  		"time": 0.9724234,
	  		"weight_difference": None,
	  		"acceleration": None
	  	},
	  	{
	  		"m1": 20,
	  		"m2": 105,
	  		"time": 0.936344,
	  		"weight_difference": None,
	  		"acceleration": None
	  	},
	  	{
	  		"m1": 15,
	  		"m2": 110,
	  		"time": 0.908686,
	  		"weight_difference": None,
	  		"acceleration": None
	  	}
	  ]
	  
	  for point in data:
	  	point['m1'] += 118.1
	  	point['m2'] += 119.2
	  	point['m1'] /= 1000
	  	point['m2'] /= 1000
	  	point['weight_difference'] = point['m2'] - point['m1']
	  	point['acceleration'] = (point['weight_difference'] / (point['m1'] + point['m2'] + 0.465/2 )) * 9.80
	  
	  weight_difference = [i['weight_difference'] for i in data]
	  accelerations = [i['acceleration'] for i in data]
	  
	  plt.scatter( np.array(weight_difference), np.array(accelerations) )
	  plt.xlabel( "Weight Difference (kg)" )
	  plt.ylabel( "Acceleration (m/s^2)" )
	  
	  trendline = np.polyfit( weight_difference, accelerations, 1 )
	  trendline_function = np.poly1d( trendline )
	  
	  little_g = trendline_function[1] * ((118.1 + 119.2 + 50 + 75 + 465/2) / 1000)
	  percent_error = abs(((little_g - 9.80) / 9.81 ) * 10)
	  print( f"Calculated little G: {little_g} | Percent Error: {percent_error.round(6)}%" )
	  
	  plt.plot( weight_difference, trendline_function(weight_difference) )
	  plt.title( f"Weight Difference vs. Acceleration\n{trendline_function[1].round(4)}x + {trendline_function[0]}" )
	  plt.show()
	  plt.savefig( f"foo{0+1}.png" )
	  plt.clf()
	  ```
- # Discussion
	- ### What would happen if we did not change the mass m1 at the same time as m2 ? (In other words, what if we kept m1 constant and just added mass to m2 ) Would the ultimate result change? Why or why not?
	  The ultimate results would not change, however the data would be reduced in extremity, because the weight difference would be lower. The acceleration would still be correct.
	- ### Consider the scenario of releasing the cylinder above the photogates (say 10 cm above). Would this affect the results that you would get? If so, how could you account for this effect (other than releasing the cylinder at the photogate)?
	  Yes, it would affect the results. Your time constant would not be as correct, as it would come in with a $$v_i \neq 0$$. This would lower the time to pass the second gate. You could counter this by adjusting your acceleration equation to calculate with a $$v_i\neq 0$$.
	- ### Describe what would happen if the friction within the pulley was not negligible. In other words, how would the system act if the pulley was not ideal or close to ideal?
	  It would require more of a weight difference to create a gravitational force large enough to create a net vertical force greater than zero.
- # Conclusion
  This was a fun lab! I struggled with visualizing the tension force due to mass difference, and was lost in the numbers that comes with substituting multiple equation into one another. 
  
  I do think that it's important that the issue with the string falling off the pulley and a lack of sure-fire way to slow the pulley should be addressed, as well as the weights being properly labeled. However, lab equipment is an easy fix.