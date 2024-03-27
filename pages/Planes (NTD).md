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
		- #### 5.5.E
		  Consider the surface $f(x,y)=(y-3x^2)(y-x^2)$. 
		  Note that $f(x,0)=(-3x^2)(-x^2)=(3x^4)$ and there is a min at $(0,0)$,
		  and for $f(0,y)=(y-0)(y-0)=y^2$ and there is a min at $(0,0)$ in the y=0 trace.
		  
		  $$\nabla f(x,y)=<-6x(y-x^2)+(y-3x^2)(-2x), (y-x^2)+(y-3x^2)>$$
		  We can see that $(0,0)$ is a critical point.
	- ### 5.3 - Theorem
	  \begin{equation}
	  D = 
	  \begin{vmatrix}
	  f_{xx}(x,y) & f_{xy}(x,y)\\
	  f_{xy}(x,y) & f_{yy}(x,y)
	  \end{vmatrix}
	  \end{equation}
	  
	  All possible cases:
	  i) D > 0, f_{xx} > 0, local minimum
	  ii)D > 0, f_{xx} < 0, local maximum 
	  iii) D < 0, it's a saddle point 
	  iv) D = 0, inconclusive
	- ### Gaussian Curvature and Extrema on Surfaces
	  A Gaussian Curve can be defined as the product of two surfaces.
	  
	  $$\Kappa_g=\frac{f_{xx}f_{yy}-f_{xy}^2}{(f_{xx}^2+f_{yy}^2+1)^2}$$
	  
	  **Bounded Planar**: There exists a finite distance between all point pairs in the set.
	  **Interior Point**: There is a disk centered at a point which is in the set
	  **Boundary Point**: Every disk centered at this point contains points both in and out of the set.
	  **Closed Set**: Contains all of its boundary points
	- ## Examples
		- #### 5.3.E1
		  Find all extrema of $f(x,y)=2x^2+y^2+4x-4y+5$.
		  
		  $\nabla f=<4x+4,2y-4>=<4(x+1),2(y-2)>$
		  
		  Now, 
		  \begin{equation}
		  D = 
		  \begin{vmatrix}
		  4 & 0\\
		  0 & 2
		  \end{vmatrix}
		  \end{equation}
		  $$D=8 > 0$$
		  We will use the second derivative test to verify whether it falls under (i) or (ii):
		  $$f_{xx} = 4 > 0$$
		  Therefore, it is a minimum.
		- #### 5.3.E2
		  Find all extrema of $f(x,y)=x^3+y^3+3xy+3$.
		  
		  $\nabla f = <3x^2+3y,3y^2+3x>$
		  
		  Creating a systems of equations:
		  \begin{cases}
		  x^2+y = 0\\
		  y^2+x = 0
		  \end{cases}
		  
		  Substituting EQ2 into EQ1:
		  $$y^4+y=0$$
		  $$\text{so}$$
		  $$y=0 \text{ or } y =-1$$
		  
		  Plugging those points back in:
		  $$(0,0) \text{ and } (-1, -1)$$
		  
		  \begin{equation}
		  D = 
		  \begin{vmatrix}
		  6x & 3\\
		  3 & 6y
		  \end{vmatrix}
		  \end{equation}
		  $$\text{or}$$
		  $$=36xy-9$$
		  
		  $D(0,0) = -9 < 0$ (Saddle Point)
		  $D(-1,-1) = -6 < 0$ (Local Maximum)
		- #### 5.3.E3
		  Find all extrema of the "*monkey saddle*" $f(x,y)=6xy^2-2x^3-3y^4$
		  
		  $\nabla f(x,y) = <6y^2-6x^2, 12xy-12y^3>$
		  Creating a system of equations:
		  \begin{cases}
		  y^2-x^2=0\\
		  xy-y^3=0
		  \end{cases}
		  $xy=y^3$ or $x=y^2$ if $y \neq 0$ and $(0,0)$ is also critical.
		  
		  So:
		  $y^2 - y^4 = 0$ or $y^2(1 - y^2)=0$
		  so
		  $(=0 @ y = 0, 1, -1)$
		  or
		  $(0,0),(1,1),(1,-1)$
		  
		  \begin{equation}
		  D = 
		  \begin{vmatrix}
		  -12x & 12y\\
		  12y & 12x-36y^2
		  \end{vmatrix}
		  = (-12x)(12x-36y^2) - (12y)^2
		  = -144x^2+432xy^2-144y^2
		  \end{equation}
		  
		  $D(0,0) = 0$ (Inconclusive, must use traces)
		     for $x = 0$, $f(0,y) = -3y^4$
		     for $y = 0$, $f(x,0) = -2x^3$ (saddle in this trace)
		  $D(1,1) = 432-2*144 > 0$,    $f_{xx}(1,1) = -12*1 < 0$ (Local Maximum)
		  $D(1,-1) = 432 - 2*144 > 0$, $f_{xx}(1,-1) = -12*1 < 0$ (Local Maximum)
		- #### 5.3.E4
		  Find extrema, if any, of $f(x,y) = \frac{x}{y^2}+xy$.
		  
		  $$\nabla f= <\frac{1}{y^2}+y, \frac{-2x}{y^3}+x>$$
		  \begin{equation}
		  \begin{cases}
		  f_x=0\\
		  f_y=0
		  \end{cases} or 
		  \begin{cases}
		  y(\frac{1}{y^3}+1)=0\\
		  x(1-\frac{2}{y^3})=0
		  \end{cases}
		  \end{equation}
		  $$\text{so}$$
		  $$(0,-1)$$
		  $$f_{xx}=0$$
		  $$f_{xy}=\frac{-2}{y^3}$$
		  $$f_{yy}=\frac{6x}{y^4}$$
		  \begin{equation}
		  D(0,-1)=
		  \begin{vmatrix}
		  0 & 3 \\
		  3 & 0
		  \end{vmatrix}
		  = -9
		  \end{equation}
		  
		  This tells us that our point is a saddle point.
		- #### 5.3.E5
		  Consider the second derivative text applied to $f(x,y) = x^2y^2$
		  
		  $$\nabla f = <2xy^2, x^22y>$$
		  \begin{equation}
		  \begin{cases}
		  2xy^2 = 0\\
		  x^22y = 0
		  \end{cases}
		  \end{equation}
		  Here $(x,0)$ and $(0,y)$ are *all* critical points!
		  
		  \begin{equation}
		  D = 
		  \begin{vmatrix}
		  2y^2 & 4xy\\
		  4xy & 2x^2
		  \end{vmatrix}
		  \end{equation}
		  
		  Sadly, this means that if $x = 0$ or $y = 0$, the test completely fails for all points.
		  *Note: The 4th order derivative test could potentially work!*
		- #### 5.3.E6S
		  Find the smallest distance (if it exists!) from point $p = (1,1,1)$ to the cone $z = \sqrt{x^2+y^2}$
		  
		  $$f(x,y) = (x-1)^2+(y-1)^2+(\sqrt{x^2+y^2}-1)^2$$
		  $$f_{x}=2(x-1) + \frac{2x(\sqrt{x^2+y^2}-1)}{\sqrt{x^2+y^2}}=0$$
		  $$f_{y}=2(y-1) + \frac{2y(\sqrt{x^2+y^2}-1)}{\sqrt{x^2+y^2}}=0$$
		  $$\text{so}$$
		  $$\frac{1-x}{x}=\frac{1-y}{y}$$
		  $$\text{so}$$
		  $$y=x\text{ if }\nabla f = 0$$
		  $$\text{setting }y=x$$
		  $$\frac{1-x}{x}=\frac{\sqrt{2x^2}-1}{\sqrt{2x^2}}$$
		  Our only critical point is at $(\frac{2+\sqrt{2}}{4},\frac{2+\sqrt{2}}{4})$. $D > 0$ and $f_{xx} >0$, so this is a local minimum.
		- #### 5.4.E
		  Find the extreme values of $f(x,y) = 2x^2-4x+3y^2-6y+5$ over the triangle with vertices $(0,0), (3,0), (0,3).$
		  
		  $\nabla f = <4x-4, 6y-6> or <4(x-1), 6(y-1)>$
		  \begin{equation}
		  D=
		  \begin{vmatrix}
		  f_{xx} & f_{xy}\\
		  f_{xy} & f_{yy}
		  \end{vmatrix}, D(1,1) = 
		  \begin{vmatrix}
		  4 & 0\\
		  0 & 6
		  \end{vmatrix}
		  \end{equation} 
		  Therefore, we can clearly see that $(1,1)$ is a local minimum.
		  
		  Next, we apply single var. EVT over the three boundary lines of the triangle.
		  
		  * x-axis:
		  $F(x) = f(x,0) = 2x^2-4x+5$
		  $F'(x,0) = 4x - 4$
		  $(1,0)$ is a candidate.
		  * y-axis:
		  $F(y) = f(0,y) = 3y^2-6y-5$
		  $F'(y) = 6y - 6$
		  $(0,1)$ is a candidate.
		  * hypotenuse:
		  $F(x) = f(x, 3-x) = 2x^2-4x+3(3-x)^2-6(3-x)+5 = 5x^2-16x+14$$$ 
		  $F'(x) = 10x-16$$$
		  $(\frac{8}{5},\frac{7}{5})$ is a candidate.
		  
		  **Total candidates**:
		  $(1,1)$ - [Interior]
		  $(0,1), (1,0), (\frac{8}{5}, \frac{7}{5})$ - [Boundary lines]
		  $(0,0), (0,3), (3,0)$ - [Corners]
		  
		  After checking,
		  $(1,1) = 0$ is the global min and $(0,3) = 14$ is the global max.
		- #### 5.4.E2
		  Find the extreme values of $f(x,y) = x^2 - y + y^3$ over the closed unit disk.
		  
		  $\nabla f = <2x, 3^2 - 1>$ - By solving, $(0, \pm\frac{\sqrt{3}}{3})$ - Values of \frac{2}{3\sqrt{3}
-