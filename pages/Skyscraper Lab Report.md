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
  |1|123000|176000|46800|
  |2|367357|58000|15000|
  |3|533000|106000|28000|
  |4|4.0e5|1.0e5|2.6e4|
  |5|369000|94000|24000|
  *Table 1: Final resultant data extracted from each group*
- # Results
	- ## 2.1 Estimating How Many People Work in the Willis Tower
		- ### 1. Calculating the total area of the base floors of the tower
		  Length = 450ft
		  Width = 450ft
		  
		  With this information, we can calculate the area in $$\text{ft}^2$$:
		  $$450\text{ft} * 450\text{ft} = 202500\text{ft}^2$$
		  
		  However, we need the area in meters:
		  $$202500ft^2*(\frac{12in}{1ft})^2*(\frac{2.54cm}{1in})^2*(\frac{1m}{100cm})^2=19000m^2$$
		- ### 2. Estimating how much of the space is actually usable. 
		  I estimate roughly only $$\frac{14}{18}$$ of the first floor is actually usable.
		  
		  Therefore, we can calculate the usable area as follows:
		  $$19000m^2*\frac{14}{18}=15000m^2$$
		- ### 3. Estimating the amount of floors in each section of the building + calculating the total available surface area in the building. 
		  
		  For the sake of the problem, I will assume that parts of the building *not* visible are eliminated/present via any symmetrical chunks.
		  
		  I will split each set of like floors into their multiplied 'actual available area'. I will also assume only a third is actually usable past that.
		  $$15000m^2 * (50 * \frac{9}{9} + 20 * \frac{7}{9} + 20 * \frac{5}{9} + 20 * \frac{2}{9}) * \frac{1}{3} = 4.1*10^5m^2$$
		- ### 4. Estimating the size of a cubicle that a person would need to work comfortably and efficiently
		  I believe that most people need around 2 meters both in width and length to work properly.
		  
		  This gives us the following area per cubicle:
		  $$2.0m*2.0m=4.0m^2$$
		- ### 5. Calculating the total number of workers
		  We can do this by dividing the usable area by the area per cubicle:
		  $$4.1*10^5m^2*\frac{1worker}{4m^2}=1.0*10^5 \text{workers}$$
	- ## 2.2 Calculating the Water Usage
		- ### 1. Calculating the total water usage per day
		  We can do this by converting the number of workers to the number of liters as follows:
		  $$1.0*10^5workers*\frac{100gallons}{1worker}=10*10^7gallons/day$$
		- ### 2. Converting to liters per minute
		  $$1.0*10^7gallons/day*\frac{1day}{24hr}*\frac{1hr}{60mins}*\frac{1m^3}{264gallons}*\frac{1000liters}{1m^3}=26000liters/min$$
- # Discussion
  I believe that the area of the base I calculated is relatively accurate, since the numbers are pulled from their website, and the only way to have error would be small portions that could jutt in or out. 
  
  However, I do have concerns with how I calculated the usable area, as 7/9th (or 14/18ths) of a given floor being usable is a serious estimate. There are many factors, such as breathing room for cubicles and the walkways between them, lounges, etc.
  
  Not knowing the size of cubicles also drastically reduces the accuracy and ability to calculate the number of employees, however, because the Willis Tower states there are 15000 employees, and by my estimates I calculated around 10000. This could be because I chose a different cubicle size, but I also believe I should have been more lenient with my multiplier of available space (currently 1/3rd), as only a third of a floor being usable is a bit of a rough estimate.
  
  In relation to calculating the actual daily water usage, I don't see how a worker could use 100 gallons of water a day in the slightest. Maybe 2-10 gallons, accounting for water fountains; sinks; and restrooms, but not 100. Therefore, I do not believe that the total water usage is accurate.
  
  However, there was another group which was completely separate from us, and reached a very similar final answer. This leads me to believe that our reasoning and final answer are sound considering the information we were provided.
- # Conclusion
  I enjoyed overcoming my fear of converting units. It was previously something I hated from AP Chem, and never worked out, but I was able to deduce my own quick method of converting units while maintaining readability and usability. I did not particularly enjoy having to 'create' constants, as this leaves significant room for error. It also eliminates the ability to differentiate between errors when comparing to other people, unless you choose to agree on constants.
  
  There was no theory for this lab, but the objectives provided were all completed.