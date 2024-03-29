public:: true

- ### Metadata
  Date: *October 10, 2023*
  Class: *PHYS253 - Section 1*
  Author: *John White*
  Professor: *Jarod Adelman*
- # Theory
	- ## Primary Objectives
	  In this lab, we will...
	  * Practice equation substitution to solve for different variables in terms of other variables
	  * 
	  * Calculate the error percentages between a calculated and measured value
- # Data
  **Ball Weight:** 130.3g
  **Ring Weight:** 23.3g
  **Cylinder Weight:** 67.9g
  
  **Distance Between Photogates:** 43.0cm
  
  **Distance Across Ball:** 3.2cm
  **Distance Across Ring:** 3.3cm
  **Distance Across Cylinder:** 3.3cm
  |Object|Gate 1 State 1|Gate 1 State 0|Gate 2 State 1|Gate 2 State 0|
  |Ball|0.4746|0.6772|1.4980|1.5334|
  |Ring|0.8819 and 1.0536|0.9135 and 1.0757|2.0596 and 2.0561|2.0256 and 2.0611|
  |Cylinder|1.0863|1.2660|2.1207|2.1588|
  
  |Object|$\Delta t_1$|$\Delta t_2$|
  |Ball|0.2026|0.0354|
  |Ring|0.1938|0.0015|
  |Cylinder|0.1797|0.0381|
  
  |Object|$\omega_1$|$\omega_2$|
  |Ball|9.8717|56.497|
  |Ring|10.320|1333.3|
  |Cylinder|11.130|52.493|
- # Results
	- ## 3.1-2 Inertia Table
	  |Object|Calculated Inertia|Thereoretical Inertia|
	  |Ball|4.38834e-5|5.337088e-5|
	  |Ring|0.0924555|0.1124225|
	  |Cylinder|3.11535e-5|3.697155e-5|
	- ## 3.2 Percent Error
	  |Object|Percent Error|
	  |Ball|17.8%|
	  |Ring|17.7%|
	  |Cylinder|21.6%|
- # Discussion
  I calculated the Inertia table's experimental values using **Equation 6**: ($$\frac{2mg(h_f-h_i)}{\omega^2_i+\omega^2_f}-mR^2$$). The standard, theoretical moments of inerta can be found with different equations depending on the type of object.
  
  The cylinder requires the following equation:
  $$I_{CM}=\frac{1}{2}MR^2$$
  The ring requires the following equation (the R values being the radius, inner and outer): 
  $$I_{CM}=\frac{1}{2}M(R^2_1+R^2_2)$$
  The sphere requires the following equation:
  $$I_{CM}=\frac{2}{5}MR^2$$
  
  The percentage error between the two was calculated with the standard percent error equation:
  $$\%_{\text{error}}=\frac{|\text{Theoretical}-\text{Experimental}|}{\text{Theoretical}}*100\%$$
  
  The high percent error is of note. I believe that while this can be due to human error (slight nudges on the object, etc), this is primarily due to the torque force applied by friction and error resistance, as our percent errors are well clustered. Our 'slide' was a little dusty, which has a high frictional constant relative to the object being slid down the ramp. This could have be remedied with some form of lubricant.
- # Conclusion
  This was an interesting lab that demonstrated how the form factor of an object does or does not affect the moment of inertia, and gave me a greater understanding of just what inertia actually means. Prior, I did not understand linear (let alone rotational) inertia.
  
  This also helped me understand just what friction is on a rolling object, and how it applies a torque force to slow such an object down.
  
  I do believe that, like all kinematic/force labs, there are issues with system factors doing entropial work on the object. There is little to be done about it, however.
  
  As a whole, I enjoyed this lab, and I would like to thank the TA for his excellent job going over how each equation is derived. It's easy to look at a complete proof with a blank stare and decide to instead 'black box' the equations, but having a fundamental understanding of each equation and what they mean and do improved my lab and final exam performance.