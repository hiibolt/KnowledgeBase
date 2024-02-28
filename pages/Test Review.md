## Horse Problem
	- ### Assumptions
	  * All horses are geometrically similar.
	  * All horses have the same density.
	- ### Equations
	  $$V\propto l^3$$
	  $$V\propto W$$
	  $$\text{so}$$
	  $$V\propto W\propto l^3$$
	  $$W=kl^3$$
	- ### Example
	  We are given one horse to be 4ft tall and weighs 800.
	  
	  From this, we can derive k:
	  $$800=k(4)^3 \text{ or } k=\frac{25}{2}$$
	  
	  We must now model the height of a 1200 pound horse:
	  $$1200=\frac{25}{2}l^3$$
	  $$\text{or}$$
	  $$l=(\frac{1200*2}{25})^\frac{1}{3}=\sqrt[3]{96}=4.58$$
- ## Repair Stations
  We have five stations ($S_i$) from west to east.
  Each station has an assigned number of visits ($N_i$)
  
  We must find the optimal station to place the repair station at.
	- ### Example
	  $(S_i, N_i): \{(1,2), (2,5), (3,3), (4,4), (5,7)\}$
	  
	  Find the slopes:
	  $$S_0=-(N_1+N_2+N_3+N_4+N_5)=-21$$
	  $$S_1=S_0+2N_1=-17$$
	  $$S_2=S_1+2N_2=-7$$
	  $$S_3=S_2+2N_3=-1 \text{ (negative slope!)}$$
	  $$S_4=S3+2N_4=7 \text{ (positive slope!)}$$
	  
	  We can see that the slope changes from negative to positive in the range of  $S_3 \text{ to } S_4$, meaning that the PDC should be positioned at the fourth station due to it being at a point of absolute minimum for the cost function.
	  
	  **Extension**
	  At what value of $N_1$ would the PDC move westward?
	  
	  $$S_0=-(N+N_2+N_3+N_4+N_5)=-19-N$$
	  $$S_1=S_0+2N=-19+N$$
	  $$S_2=S_1+2N_2=-9+7$$
	  $$S_3=S_2+2N_3=-3+N$$
	  
	  Previously, $S_3 < 0$. With a $N >= 3$