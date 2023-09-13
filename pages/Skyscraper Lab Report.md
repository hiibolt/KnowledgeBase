## Metadata
Date: *September 12, 2022*
Class: *PHYS253 - Section 1*
Author: *John White*
Professor: *Jarod Adelman*
- # Theory
	- ## Primary Objectives
	  * Learn to convert between typical units while adhering to the laws of significant figures
	  * Determine the number of people working in the Willis Tower
	  * Calculate the water usage of the Willis Tower in liters per minutes.
- # Data
  |Group|Usable Area ($$m^2$$)|Workers|Water Usage ($$\frac{liters}{min}$$)|
  |------|:------------------------:|:-------:|-------------------------------------:|
  |1||||
  |2||||
  |3||||
  |4||||
  |5||||
  *Table 1: Final resultant data extracted from each group*
- # Results
	- ## 2.1 Estimating How Many People Work in the Willis Tower
		- ### 1. Starting with the length and width of the ground floor provided, calculate the total area in meters.
		  Length = 450ft
		  Width = 450ft
		  
		  With this information, we can calculate the area in $$\text{ft}^2$$:
		  $$450\text{ft} * 450\text{ft} = 202500\text{ft}^2$$
		  
		  However, we need the area in meters:
		  $$202500ft^2*(\frac{12in}{1ft})^2*(\frac{2.54cm}{1in})^2*(\frac{1m}{100cm})^2=19000m^2$$
		- ### 2. Use Figure 1 to estimate how much of the space that you calculated is actually usable. 
		  I estimate roughly only $$\frac{14}{18}$$ of the first floor is actually usable.
		  
		  Therefore, we can calculate the usable area as follows:
		  $$19000m^2*\frac{14}{18}=15000m^2$$
		- ### 3. Use Figure 2 to estimate the amount of floors in each section of the building and calculate the total available surface area in the building. 
		  
		  For the sake of the problem, I will assume that parts of the building *not* visible are eliminated/present via any symmetrical chunks.
		  
		  I will split each set of like floors into their multiplied 'actual available area'. I will also assume only a third is actually 
		  $$15000m^2 * (50 * \frac{9}{9} + 20 * \frac{7}{9} + 20 * \frac{5}{9} + 20 * \frac{2}{9}) * \frac{1}{3} = 41000m^2$$
		- ### 4. Estimate the size of a cubicle that a person would need to work comfortably and efficiently.
		  I believe that most people need around 2 meters both in width and length to work properly.
		  
		  This gives us the following area per cubicle:
		  $$2m*2m=4m^2$$
		- ### 5. Using your estimation from Step 4, calculate the total number of workers in the Willis Tower.
		  We can do this by dividing the usable area by the area per cubicle:
		  $$41000m^2*\frac{1worker}{4m^2}=10*10^3 \text{workers}$$
	- ## 2.2 Calculating the Water Usage
		- ### 1. Using the given that city planners assume that each person uses 100 gallons of water per day and your results from Part 1, calculate the total water usage per day in the Willis Tower.
		  We can do this by converting the number of workers to the number of liters as follows:
		  $$10*10^3workers*\frac{100gallons}{1worker}=10*10^5gallons/day$$
		- ### 2. Convert your result in Step 1 from gallons per day to liters per minute.
		  $$10*10^5gallons/day*\frac{1day}{24hr}*\frac{1hr}{60mins}*\frac{1m^3}{264gallons}*\frac{1000liters}{1m^3}=2600liters/min$$
- #