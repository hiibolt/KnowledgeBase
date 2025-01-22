## Chapter 1
	- ### Definitions
	  * **Statistics** is the science of gathering data to help draw a conclusion based on said data
	  * **Population** is a collection of objects
	  * **Census** is a method of gathering that surveys *all* candidates.
	  * **Study/Sample Survey** is gathering information from a smaller subset of candidates.
	  * A **variable** is a characteristic that is variadic in nature. These use capital letters. For the actual data, use the lowercase equivalent of them.
	  * A **univariate, bivariate dataset** is a dataset consisting of just one and two variables respectively. A **multivariate dataset** is a dataset consisting of two or more variables.
	  * A **sample space** is the set of all possible outcomes of an experiment. 
	    *Use set builder notation if possible*.
	- #### Types of Variables
		- #### Quantitative 
		  A *measure* of something.
			- #### Discrete
			  Does not span a number line.
			- #### Continuous
			  Spans a number line in its entirety.
		- #### Qualitative
		  A *description* of something.
	- ## Graphs
		- ### Histograms
		  A graph of *quantitative discrete* data.
		  
		  The **relative frequency** of a data count $x$ with set size $n$ is $\frac{x}{n}$.
		  The **frequency** distribution is a table with three headers:
		  * *Data Type*
		  * *Frequency*
		  * *Relative Frequency*
			- #### Modality
			  A *unimodal* graph has one mode, a *bimodal* graph has two, *multimodal* graph has three, and a *uniform* graph has no model.
			- #### Skewing
			  A *skewed* graph leans either away from left or away from right, whereas a *symmetric* graph has similar left and right sides.
			  
			  Can also be thought of stretching - that makes the inverted direction make a lot more sense.
		- ### Boxplots
		  Constructed by drawing a line on a number line between the lowest and highest entry, followed by a two boxes sharing a midpoint (the set mean) and a left side of the *lower fourth* (median of the smaller half) and a right side of the *upper fourth* (median of the upper half).
		  
		  It's worth noting that they can also display outliers by not drawing the line to certain points, instead opting to render them as filled circles (mild outliers) or no-fill circles (extreme outliers).
	- ## Dataset Indicators
		- ### Mean
		  The computational average of a set.
		  
		  Rendered as $\overline{x}$ or $\mu$.
			- #### Trimmed Mean
			  A mean where you remove $$X%$$ of the upper and lower halves of the dataset.
			  
			  For example, a 10% trimmed mean would mean calculating the mean of the dataset, exempting the highest 10% and lowest 10% data points.
		- ### Median
		  The middle value of the set if calculated on an odd dataset, or the average of the middle two values if calculated on an even dataset.
		  
		  Rendered as $\tilde{x}$ or $\tilde{\mu}$.
	- ## Measures of Variance
		- ### Range
		  The difference between the highest and lowest datapoints.
		- ### Standard Deviation
		  $$s=\sqrt{\frac{\sum_{i=0}^n(x_i-\overline{x})^2}{n-1}}$$
			- ### Population Variance
			  $$\sigma^2=\sum_{i=1}^{N}(x_i-\mu)^2/N$$
			- ### Shortcut Variance
			  $$S_{xx}=\sum{x_i^2}-\frac{(\sum{x_i})^2}{n}$$
			  
			  Note - this is an equivalent of the *numerator* of the above operations. This is not a standalone operation!