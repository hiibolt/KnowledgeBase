## Key points
Can be $\in \mathbb{R}^3$ or $\in \mathbb{R}^2$
- ## 5 - Directional Derivatives
  $$\lim_{h->0}\frac{f(x_0+h\cos(\theta),y_0+h\sin(\theta))-f(x_0,y_0)}{t}$$
  $$\text{For a unit vector } u=<u_1,...,u_n>$$
  $$\lim_{t->0}=\frac{f(x+tu)-f(x)}{t}$$
	- ### 5.1 - Thereom
	  $$\text{For a unit vector }u=<a,b>$$
	  $$D_uf(x_0,y_0)=f_x(x_0,y_0)a+f_y(x_0,y_0)b$$
		- #### 5.1.E
		  For $f(x,y) = x^2y+2xy^3$ calculate, and interpret, the directional derivative of f at (1,2) in the direction of $v=<2,3>$
		  
		  **Solution**:
		  $$20*(\frac{2}{\sqrt{13}})+25*(\frac{3}{\sqrt{13}})$$
	- ### 5.2 - Gradients
	  'The vector of partial derivatives $\nabla f(x,y,...,n) = <f_x, f_y,...,f_n>$'
	  In other words, when asked for a gradient, provide $\nabla f$
	  
	  Or, more generally,
	  $$\text{For a unit vector } u \text{ at } x_0 \text{,}$$
	  $$D_u f(x_1,...,x_n)=\nabla f(x_0)*u$$
	  
	  
	  Which has an interesting property that the maximum value of the gradient is the positive norm of nabla f ($||\nabla f||$), and the minimum value is the same but negative ($-||\nabla f||$). 
	  
	  Considering this involves a dot product, this is proven by the maximum value being at $\theta = 0$ and the minimum value being at $\theta = \pi$.
		- #### 5.2.E
		  Find the minimum/maximum values of $D_uf$ for $f(x,y)=x^5+xy^3+y^3$ at the point $(1,1)$.
		  
		  $$\nabla f=<5x^4+y^3,3xy^2+3y^2>$$
		  $$\nabla f=<6,6>$$
		  $$u=\pm\frac{\nabla f(1,1)}{||\nabla f(1,1)||}=\pm\frac{1}{\sqrt{36+36}}<6,6>=\pm<\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}}>$$
		  
		  Thus, the directional derivative is minimized at 
		  $u=< -\frac{1}{\sqrt{2}}, -\frac{1}{\sqrt{2}}>$, $Du_1f(1,1)=-\sqrt{72}=-6\sqrt{2}$
		  and maximized at 
		  $u=<\frac{1}{\sqrt{2}},\frac{1}{\sqrt{2}}>$, $Du_2f(1,1)=6\sqrt{2}$
		- #### 5.2.E
		  Calculate the directional derivative of $f(x,y)=x^3\cos(2y) at (1,\frac{\pi}{2})$ in the direction of $v=<3,4>$ and compare this to the minimum and maximum values of the directional derivative $D_uf$
	- ###
-