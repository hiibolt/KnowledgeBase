### Metadata
Date: *September 21, 2022*
Class: *PHYS253 - Section 1*
Author: *John White*
Professor: *Jarod Adelman*
- # Theory
	- ## Primary Objectives
	  * ~~
	  * ~~
	  * ~~
- # Data
	- ## 2.1 Coin Toss
	  I will be omitting the data section, as the data is both generated and used procedurally in a single run. Please see **3.1 Coin Toss** for an in-depth explanation.
	- ## 2.2 Table Measurements
	  Length: 92.3\plusmn0.1cm
	  Width: 183.8\plusmn0.1cm
- # Results
	- ## 3.1 Coin Toss
		- ### 3.1.1 Data Template
		  I first decided to omit the manual entry nature, I would rather instead calculate new data on each run - this helps to omit outliers.
		  
		  I started with an array (list, for python'ers), with an entry for each of the 4 experiments. I accordingly titled it ``experiments``.
		  
		  For each entry of ``experiments`` (each experiment, if you will), I included an object (dict, in python). There are 2 constants: ``total_trials``; which is the number of trials to run for that experiment, and ``total_tosses``; which is the number of tosses for each trial. There is also an array (list) adequately titled ``trial_outcomes``, which is an array to which each result from each trial is appended to.
		  
		  After filling in the constants according to the lab, this is the resulting dataset template:
		  ![image.png](../assets/image_1695230604670_0.png)
		- ### 3.1.2 Data Generation
		  Now, to populate each of the ``trial_outcomes``, we must first iterate each experiment. Following this, we must iterate through each trial. And finally, we must iterate through each coin toss, and add the resulting coin toss to a counter.
		  
		  After the final coin toss, this counter is appended to its corresponding ``trial_outcomes``.
		  
		  The code for this section looks as such:
		  ![image.png](../assets/image_1695230775911_0.png)
		- ### 3.1.3 Calculating the Averages
		  For each dataset, I am required to present the average between all trials per experiment.
		  
		  Logically, to do so, we must first iterate each experiment, and then calculate after the data is generated. Therefore, I place the calculation in the first level loop after the data is found.
		  
		  Calculating the average itself is as simple as adding all elements of the ``trial_outcomes`` and dividing by the number of flips, which is ``total_trials * total_tosses``.
		  
		  In Python, using the ``reduce`` function on a list reduces each element to a starting accumulator. By using a basic ``lambda`` function which adds each new element to said accumulator, the following code correctly calculates the average ()and stores it in ``average`` for later data logging):
		  ![image.png](../assets/image_1695231114076_0.png)
		- ### 3.1.4 Calculating the Standard Deviation
		  We can start by calculating the bottom half of the inner fraction of the formula for standard deviation. This is accomplished by subtracting 1 from the total number of tosses, ``total_trials * total_losses``.
		  
		  Accordingly: 
		  ![image.png](../assets/image_1695231227676_0.png)
		  
		  Next, to calculate the deviation itself, we must take the sum of each element minus the average square. Here, I use the same ``reduce`` function from before to do so - it calculates that formula and adds it to the accumulator.
		  
		  Finally, we must take the ``sqrt`` of the top divided by the bottom. Our final code follows:
		  ![image.png](../assets/image_1695231357087_0.png)
		- ### 3.1.5 Logging
		  Last, we need a way to interpret this data. I accomplish this with basic usage of the print function and Python's (strange) syntax for string interpolation, and some escape characters for sake of line numbers:
		  ![image.png](../assets/image_1695231434298_0.png)
		  *Note: The print statements are split in favor of taking the screenshot.*
		- ### 3.1.6 Final Code and Results
		  **Code:**
		  ![image.png](../assets/image_1695231733222_0.png) 
		  **Results:**
		  ![image.png](../assets/image_1695230188595_0.png){:height 656, :width 713}
	- ## 3.2 Table Measurements
		- ### 1.) Calculating the Perimeter and Area
		  Perimeter = 552.2cm (gains a sigfig from addition)
		  Area = 1.70e4cm
		- ### 2.) Calculating the Uncertainties
		  **Perimeter:** 
		  $$\sigma_{perimeter}=\sqrt{(0.1cm)^2+(0.1cm)^2}=\sqrt{0.01cm^2+0.01cm^2}=\sqrt{0.02cm^2}=0.14cm$$ 
		  **Area:**
		  $$\sigma_{area}=(1.70e4cm^2)\sqrt{(\frac{0.1cm}{92.3cm})^2+(\frac{0.1cm}{183.8cm})^2}=20cm^2$$
- # Discussion
  **Coin Toss**:
  I was first tasked with generating **4 sets of data** for later usage. However, I think this adds an unnecessary level of error-prone manual entry. As a result, I decided to instead generate the data on the fly for each different run of the program. Therefore, my results can be run multiple times to create a better picture of the random nature of the experiment. 
  
  I was next tasked with finding the **average** of the datasets, which I do so by adding each element together. Here, it is worth noting that I use Python's embedded library ``functools.reduce``, as it is far more optimized than using manual iteration with an accumulator. This allows me to, combined with Python's ``lambda`` syntax, makes for a clean and readable one-line sum function. I also enjoy using new methods of coding in general.
  
  Next, I was tasked with finding the **standard deviation**. I accomplish this with the same ``functools.reduce`` approach,
- # Conclusion
  ~~