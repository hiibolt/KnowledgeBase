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
	  $$S_1=S_0+2N_1=$$
	  $$S_2=S_1+2N_2$$