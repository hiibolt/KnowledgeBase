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
	  
	  **Special Properties**:
	  Gradients can be used to find the tangent line, plane, and more.
	  
	  For instance, for a given point $p$ on a surface defined by $F$, the tangent line at $p$ is:
	  $$l(t)=p+t(\nabla F(p)$$
	  
	  Similarly, the tangent plane can be found as:
	  $$\nabla F(p) \cdot <x - x_0, y - y_0, z - z_0> = 0$$
	  
	  Finding the tangent line at a curve of intersection for two surfaces F and G:
	  *Must first ensure the point is actually an intersection!*
	  $$l(t)=p+t(\nabla F(p) x \nabla G(p))$$
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
		  Calculate the directional derivative of $f(x,y)=x^3\cos(2y) at (1,\frac{\pi}{2})$ in the direction of $v=<3,4>$ and compare this to the minimum and maximum values of the directional derivative $D_uf$.
		  
		  Direction = $\frac{1}{\sqrt{3^2+4^2}}<3,4>=<\frac{3}{5},\frac{4}{5}>$
		  $\nabla f=<3x^2\cos(2y),-2x^3\sin(2y)>$
		  $\nabla f(1,\frac{\pi}{2})=<-3,0>$
		  Thus,
		  $$D_uf(1,\frac{\pi}{2})=\nabla f(1,\frac{\pi}{2})*u$$
		  $$\text{or}$$
		  $$=<-3,0>*<\frac{3}{5},\frac{4}{5}>=-\frac{9}{5}$$
		  Which is minimized at $u=-\frac{\nabla f(1,\frac{\pi}{2})}{||\nabla f(1,\frac{\pi}{2})||}=<1,0>$ or $D_{<1,0>}f(1,\frac{\pi}{2}=f_x(1,\frac{\pi}{2})=3$
		  Which is maximized at $u=\frac{\nabla f(1,\frac{\pi}{2})}{||\nabla f(1,\frac{\pi}{2})||}=<-1,0>$ or $D_{<1,0>}f(1,\frac{\pi}{2}=f_x(1,\frac{\pi}{2})=-3$
		- #### 5.3.E
		  Calculate the directional derivative of $f(x,y,z)=x^3yz^2\text{ at } (2,1,-1)$ in the direction of $v=<1,2,3>$ and compare this to the minimum and maximum values of the directional derivative $D_uf$.
		  
		  Direction = $\frac{1}{\sqrt{1+4+9}}<1,2,3>=<\frac{1}{\sqrt{14}},\frac{2}{\sqrt{14}},\frac{3}{\sqrt{14}}>$
		  $\nabla f(x,y,z)=<3x^2yz^2,x^3z^2,2x^3yz>$
		  so
		  $\nabla f(2,1,-1)=<12,8,-16>$
		  
		  Thus,
		  $$D_uf(2,1,-1)=\nabla f(2,1,-1)*u$$
		  $$\text{or}$$
		  $$=<12,8,-16>*<\frac{1}{\sqrt{14}},\frac{2}{\sqrt{14}},\frac{3}{\sqrt{14}}>$$
		  $$=12(\frac{1}{\sqrt{14}})+8(\frac{2}{\sqrt{14}})-16(\frac{3}{\sqrt{14}})$$
		  Which is minimized at $u=-\frac{\nabla f(2,1,-1)}{||\nabla f(2,1,-1)||}=...$ or $D_{...}f(2,1,-1)=-\sqrt{12^2+8^2+16^2}$
		  Which is maximized at $u=\frac{\nabla f(2,1,-1)}{||\nabla f(2,1,-1)||}=...$ or $D_{...}f(2,1,-1)=\sqrt{12^2+8^2+16^2}$
		- #### 5.4.E
		  Find the tangent line to the curve of intersection to the surfaces $x^2-xy+y^2-z=2$ and $x^2+y^2-z^2=1$ at $p=(1,-1,1)$.
		  
		  $$\nabla F = <2x-y, 2y-x, -1>$$
		  $$\nabla F(p) = <3,-3,-1>$$
		  $$\nabla G = <2x,2y,2z>$$
		  $$\nabla G(p) = <2,-2,-2>$$
		  $$\text{so}$$
		  $$\nabla F(p) x \nabla G(p) = <4,-4,0>$$
		  $$\text{so}$$
		  $$l(t)=p+t(\nabla P(p) x \nabla G(p)$$
		  $$=<1+4t, -1-4t, 1>$$
	- ###
-