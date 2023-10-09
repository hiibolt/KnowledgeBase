public:: true

- ### Metadata
  Date: *October 7th, 2023*
  Class: *PHYS253 - Section 1*
  Author: *John White*
  Professor: *Jarod Adelman*
- # Theory
	- ## Primary Objectives
	  In this lab, we will...
	  * Learn to use Python's graphing library, matplotlib
	  * Learn to draw trendlines and annotate R^2
	  * Learn the relationships between data, their trendlines, and what the trendlines represent
- # Data
	- ## 2.1 Data For Each Angle
		- ### 2.1.1 Angle 1
		  ![image.png](../assets/image_1696882381416_0.png)
		- ### 2.1.2 Angle 2
		  ![image.png](../assets/image_1696882411066_0.png)
		- ### 2.1.3 Angle 3
		  ![image.png](../assets/image_1696882435470_0.png)
- # Results
	- ## 3.1 Analyzing the Angle Data
		- ### 3.1.1 Creating the Graph Generation Code
			- ### 3.1.1.1 Calculating the Angles
			  I calculate each of the angles using the following equation: 
			  $$arctan(\frac{h_2-h_1}{l})=\theta$$
			  
			  This data can be seen above in the ``angle`` field of each experiment.
			  
			  I structured my data in the following pattern:
			  **First:** ``experiments`` is an array of each ``angle``'s experiments.
			  **Second:** Each ``experiment`` contains an ``angle`` and a ``trials`` field.
			  **Third:** ``trials`` is an array of ``trial`` objects, containing a ``time``, ``position``, and ``velocity`` data array.
			- ### 3.1.1.2 Create Graphs For Position vs. Time and Velocity vs. Time
			  I accomplish this with the ``matplotlib`` library. 
			  
			  First, I iterate each of the experiments and trials: (I set aside the angle for later usage)
			  ![image.png](../assets/image_1696883587851_0.png)
			  
			  Then, I build a basic graph for each: 
			  ![image.png](../assets/image_1696883629848_0.png)
			  ![image.png](../assets/image_1696883645392_0.png)
			- ### 3.1.1.3 Create a Trendline And Calculate $R^2$
			  I do this using the ``sklearn`` library, as they have a built-in $$R^2$$ function. I then plot them both.
			  
			  I use a polynomial line of degree 1, because while a second degree would be more accurate, I instead prefer the ease of calculation because the difference between the two in visual line representation is negligible.
			  
			  I then include both figures in the title of the graph.
			  ![image.png](../assets/image_1696883920786_0.png)
			- ### 3.1.1.4 Calculating Little G
		-
- # Discussion
  **Coin Toss**:
  I was first tasked with generating **4 sets of data** for later usage. However, I think this adds an unnecessary level of error-prone manual entry. As a result, I decided to instead generate the data on the fly for each different run of the program. Therefore, my results can be run multiple times to create a better picture of the random nature of the experiment. 
  
  I was next tasked with finding the **average** of the datasets, which I do so by adding each element together. Here, it is worth noting that I use Python's embedded library ``functools.reduce``, as it is far more optimized than using manual iteration with an accumulator. This allows me to, combined with Python's ``lambda`` syntax, makes for a clean and readable one-line sum function. I also enjoy using new methods of coding in general.
  
  Next, I was tasked with finding the **standard deviation**. I accomplish this with the same ``functools.reduce`` approach, taking each element; subtracting the average; squaring the result; and adding the final result to the built in accumulator. I finally divide by the lower half of the fraction, which I labeled N, although technically it's N - 1.
  
  The resulting data and the statistics gleaned from them do in fact line up with a rough 50% average heads (skewed one way or another slightly), and the standard deviations are low enough to not raise flags.
  
  **Table Measurements**:
  I was first asked to measure the table, and I **eyeballed** the final digit. I dislike the idea of having to eyeball, but I understand that ironically it can add more accuracy to a given measurement.
  
  Next, I found the directly computed perimeter and area, with no standard deviation. I have no comments on this step, it is basic usage of the formulas $$a = w*h$$ and $$p=2w+2h$$.
  
  Finally, I tackled calculating the **error propagation**. My resulting values were around the final answers I predicted, especially the area. I will be frank and state that I do not understand how the error propogation formula for area was derived.
- # Conclusion
  I enjoyed this lab, and it was refreshing to use Python for the first time in a long while. I can't say I enjoy using it, but it's hard not to appreciate how little has to be written. It's prone to developer error and slow, but perfectly suited for fast statistical and mathematical computations. I did not enjoy the table section because I did not understand how the error propagation formulas were derived.
  
  I believe the theory was satiated.
  
  I used Python frequently prior, so considering that leaning it was likely the point of the lab, it's hard to say that I learned something substantial. I do think the lab was a success for others, as they seemed to learn a lot about Python through the slides linked on the course material section. I would add more explanation regarding the derivation of the error propagation formulas.