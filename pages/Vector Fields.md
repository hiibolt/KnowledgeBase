## Definition
A vector field is **conservative** if it is the gradient of some differentiable function $f$, that is, $F = \nabla f$.
- ### Example Setup
  Take a smooth planar curve $$C(t) = (x(t),y(t))$$ for $$a \leq t \leq b$$. 
  
  Then partition $$[a,b]$$ $$n$$ ways with $$a=T_0<t_1<t_2<...<t_n=b$$ and choose sample points $$t_i^{*}\in [t_{i-1},t_i]$$.
  
  Then take $$p_i^{*}=C(t_i^{*})=(x(t_i^{*}),y(t_i^{*})):=(x_i^{*},y_i^{*})$$
  This will be a sample point in the *image* of $[t_{i-1},t_i]$ on the curve $C$.
  
  Then, take a Riemann sum.
  $$\sum_{i=1}^n f(C(t_i^{*}))\Delta S_i$$
  $$S_i=\int_{z_{i-1}}^{z_i}\sqrt{(\frac{dx}{dt})^2+(\frac{dy}{dt})^2}dt\approx \sqrt{(x'(t_i^{*}))^2+(y'(t_i^{*}))^2}\Delta t_i$$
  
  Then taking the limit:
  $$\int_C f(x,y)dS = \lim_{n\rarr\infty}\sum_{i=1}^nf(p_i^{*})\Delta S_i$$
  $$\text{or}$$
  $$=\int_a^b f(x(t), y(t))\sqrt{(\frac{dx}{dt})^2+(\frac{dy}{dt})^2}$$
  
  This can be construed as the "area under the surface", where $$z=f(x,y)$$ "over" the curve.
  
  For $$g(x,y) = f(x)$$ for $$a \leq x \leq b$$:
  $$=\int_C g(x,y) dS = \int_a^b g(t,0)\sqrt{(1)^2+(0)^2}dt$$
  $$\text{or}$$
  $$\int_a^bf(x)dx$$
  
  **N Dimension Extension**:
  $$=\int_a^b(f(x(t), y(t), z(t), ...)\sqrt{(\frac{dx}{dt})^2+(\frac{dy}{dt})^2+(\frac{dz}{dt})^2+...}$$
	- ### Example 10.1.E1
	  Evaluate $$\int_C(2x+3xy^2)dS$$ for $C$, the portion of the unit circle with $x \geq 0$.
	  
	  $$C(t) = (\cos(t),\sin(t)) \text{ over }-\frac{\pi}{2}<z<\frac{pi}{2}$$
	  
	  Then, integrate $$f(x,y) = 2x + 3xy^2$$ over $C_i$.
	  $$\int_C(f)dS = \int_{\frac{-\pi}{2}}^{\frac{\pi}{2}}((2\cos(t) + 3\cos(t) \sin^2(t))\sqrt{(-\sin(t))^2+(\cos (t))^2})dt$$
	  $$\text{or}$$
	  $$= \int_{\frac{-\pi}{2}}^{\frac{\pi}{2}}(2\cos(t) + 3\cos(t) \sin^2(t))dt$$
	- ### Example 10.1.E2
	  Evaluate the line integral $$\int_C(2x+9z)ds$$ for $C$ the twisted cubic, which we defined as $$C(t) = (t, t^2, t^3)$$ for $$0 \leq t \leq 1$$.
	  
	  $$=\int_C(f)ds=\int_0^1(2(t)+9(t^3))\sqrt{1+9t^2+9t^4}$$
	  $$\text{or (u-sub)}$$
	  $$=\int_{u(0)}^{u(1)}(u^{\frac{1}{2}})du=\int_1^{14}(\frac{u^{\frac{1}{2}}}{4})du$$
	  $$\text{or}$$
	  $$=\frac{1}{6}(14^{\frac{3}{2}}-1)$$
- ### Piecewise Smooth Definition
  A curve is **piecewise smooth** if it is a finite union of smooth curves, and we may write:
  $$C=C_1\cup C_2\cup ... C_n$$
  
  From there, subdivide into various integrals for each section between various $$C$$s.
	- ### Example 10.2.E1
	  Evaluate $$\int_Cf(x,y)ds$$ for $$f(x,y) = x^2 + xy + y^2$$ over triangle with vertices $$(0,0), (1,0), (1,1)$$.
	  
	  $$C_1(t) = (t,0)$$
	  $$C_2(t) = (1,t)$$
	-