## General Definition
	- #### 6.1.E1
	  Evaluate $\int\int x\cos(x+2y)dA$ for $R = [0,\frac{\pi}{2}] * [0,\pi]$
	  
	  $$\int (x\sin(x+2y)+\cos(x+2y)|_0^{\frac{\pi}{2}})$$
	  $$\text{or}$$
	  $$\int (\frac{\pi-2}{2}cos(2y) - sin(2y))dy$$
- ## General Areas
  Use a new function F:
  \begin{cases}
  f(x,y)\text{ if }(x,y) \in D\\
  0\text{ if }(x,y) \notin D
  \end{cases}
  
  Then:
  $$\int\int F(x,y) dA$$
	- ### 6.2.E1
	  $$=\int_0^1\int_0^{x^3}cos(x^4)dydx$$
	  $$\text{or}$$
	  $$=\int_0^1y\cos(x^4)|_0^{x^3}dx$$
	  $$\text{or}$$
	  $$=\int_0^1x^3\cos(x^4)dx$$
	  $$\text{or (u-sub)}$$
	  $$\text{...}$$
	- ### 6.2.E2
	  Evaluate $$\int\int_Dx^2y^2dA$$ for 
	  \begin{equation}
	  D = 
	  \begin{cases}
	  (x,y) | \frac{y}{2} \leq x \leq \sqrt{y}, 0 \leq y \leq 4
	  \end{cases}
	  \end{equation}
	  
	  Our box is $(0,2)$ for $x$, and $(0,4)$ for $y$.
	  
	  $$\int_0^4\int_0^2 F(x,y)dA$$
	  $$\text{or}$$
	  $$\int_0^4\int_{\frac{y}{2}}^{\sqrt{y}} x^2y^2 dxdy$$
	  $$\text{or}$$
	  $$\int_0^4 \frac{x^3}{3}y^2|_{\frac{y}{2}}^{\sqrt{y}}dy$$
	  $$\text{or}$$
	  $$\int_0^4(\frac{y^\frac{7}{2}}{3}-\frac{y^5}{24})dy$$
	  $$\text{(latter half is arithmetic, no deviation from Calc II)}$$
	- ### 6.2.E3
	  Integrate $f(x,y) = 2x+3y+4$ over the unit disk.
	  
	  \begin{equation}
	  D = \{(x,y) | -1 \leq x \leq 1, -\sqrt{1-x^2} \leq y \leq \sqrt{1-x^2} \}
	  \end{equation}
	  $$\int_{-1}^1\int_0^1(2x+3y+4)dxdy$$
	  $$\text{or}$$
	  $$\int_{-1}^1\int_{-\sqrt{1-x^2}}^{\sqrt{1-x^2}}(2x+3y+4)dxdy$$
	  $$\text{or}$$
	  $$\int_{-1}^1[2xy+\frac{3}{2}y^2+4y]|_{-\sqrt{1-x^2}}^{+\sqrt{1-x^2}}dx$$
	  $$\text{or}$$
	  $$\int_{-1}^1(4x\sqrt{1-x^2}+8\sqrt{1-x^2})dx$$
	  $$\text{or}$$
	  $$2\int_0^1(8\sqrt{1-x^2})dx$$
	  $$\text{or}$$
	  $$8\pi$$
	- ### 6.2.E4
	  Integrate $f(x,y) = e^{x^2}$ over the triangle with vertices $(0,0), (1,0), and (1,1).$
	  
	  $$D=\{(x,y) | 0 \leq x \leq 1, \}$$