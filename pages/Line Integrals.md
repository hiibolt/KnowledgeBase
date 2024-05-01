## Definition
$$\int_C f(x,y) dx = \lim_{n\rarr\infty}\sum_{i=1}^{n}f(x(t^{*}),y(t^{*}))\Delta x_i$$

For a line integral for space curve $C$ with $$a\leq t \leq b$$,
$$\int_Cf(x,y,z) = \int_a^b(f(x(t),y(t),z(t))x'(t))dt$$
$$\int_Cf(x,y,z) = \int_a^b(f(x(t),y(t),z(t))y'(t))dt$$
$$\int_Cf(x,y,z) = \int_a^b(f(x(t),y(t),z(t))z'(t))dt$$
$$\text{so}$$
$$\int_CPdx+Qdy+Rdz$$

When integrating each over the scalar components of a field:
$$F(x,y,z) = <P(x,y,z), Q(x,y,z), R(x,y,z)>$$

**Theorem**:
Let $$C$$ be a curve with domain $$a\leq t\leq b$$, (of any dimensions):
$$\int_Cfds = \int_{-C}fds \text{ and } \int_Cfdu = -\int_{-C}fdu$$

**Work Formulas**:
$$W=\int_CF\cdot Tds$$
$$\text{or}$$
$$W=\int_CPdx+Qdy+Rdz$$

**FTC for Line Integrals**:
$$\int_C\nabla f\cdot dr=f(r(b))-f(r(a))$$
	- ## Green's Theorem
	  id:: 66324325-c13a-47b6-92fe-4e5215b7077b
	  $$\oint^\uarr_CPdx+Qdy = \int\int_D(\frac{dQ}{dx}+\frac{dP}{dy})dA$$
- ## Example 11.1.E1
  Evaluate $$\int_C P(x,y)dx, \int_C Q(x,y)dy$$ and $$\int_C(P(x,y) + Q(x,y))dy$$ for $$P(x,y) = x+2y$$ and $$Q(x,y) = 2x^2 - 5xy$$ for $$C(t) = (t,t^2)$$ with $$0\leq t\leq 1$$
  
  $$\int_CPdx = \int_0^1(t+2t^2)(1)dt=\frac{7}{6}$$
  $$\int_CQdy = \int_0^1((2t^2-5t(t^2))(2t))dt=-1$$
  $$\text{so}$$
  $$\int_C(Pdx+Qdy) = \frac{7}{6}-1 = \frac{1}{6}$$
- ## Example 11.1.E2
  Evaluate $$\int_CPdx+Qdy+Rdz$$ for $$P(x,y,z) = 2x-xy$$, $$Q(x,y,z) = xy$$, $$R(x,y,z) = z^2$$ along the helix curve $$C(t,) = (\cos t, \sin t, t)$$ with $$0\leq t \leq 2\pi$$.
  $$\int_CPdx+Qdy+Rdz=\int_0^{2\pi}((2\cos t - \cos t \sin t)(-\sin t))dt$$
  $$+\int_0^{2\pi}(\cos t \sin t\cos t)dt + \int_0^{2\pi}(t^2)dt$$
- ## Example 11.1.E3
  Find the work done by the field $$F(x,y) = <xy, x^2y^2>$$ in moving a particle over the quarter circle $$r(t) = (\cos(t),\sin(t))$$ for $$0\leq t\leq \frac{\pi}{2}$$.
  
  $$W=\int_0^{\frac{\pi}{2}}F(r(t))\cdot r'(t)dt$$
  $$\text{or}$$
  $$=\int_0^{\frac{\pi}{2}}<\cos t\sin t,\cos^2 t\sin^2 t>\cdot < -\sin t, \cos t>dt$$
  $$\text{or}$$
  $$=\int_0^{\frac{\pi}{2}}(-\sin^2 t\cos t+\cos^3 t\sin^2 t)dt$$
  $$=-\frac{1}{5}$$
- ## Example 11.1.E4
  Find the work done by the force field $$F(x,y) = <z,x,-y>$$ in moving a particle along the twisted cubic $$r(t) = (t, t^2, t^3)$$ for $$0 \leq t \leq 1$$.
  
  $$W=\int_C Pdx + Qdy + Rdz = \int_0^1(t^3)(1)dt+\int_0^1(t)(2t)dt+\int_0^1(t^2)(3t^2)dt$$
  $$\text{or}$$
  $$=\frac{1}{4}+\frac{2}{3}-\frac{3}{5}$$
- ## Example 11.2.E1
  Find the work done by Newton's gravitational field, which we defined as the vector field $$F(x,y,z) = -\frac{mMg}{(x^2+y^2+z^2)^\frac{3}{2}}<x,y,z>$$ in moving an object from the point $$p=(3,1,4)$$ to the point $$q=(6,3,5)$$.
  
  $$W=\int_C F\cdot df=\int_C \nabla f \cdot dr = f(q) - f(p)$$
  $$=f(6,3,5) - f(3,1,4) = ...$$
- ## Example 11.3.E1
  Show that the vector field $$F(x,y) = \langle\frac{y}{1+x^2}+2x, \tan^{-1}(x) + 3y^2\rangle$$ is conservative and find $$f$$.
  
  $$=\int(\tan^{-1}(x) + 3y^2)dy$$
  $$\text{or}$$
  $$=y\tan^{-1}(x) + y^3 + x^2 + K$$
  
  Ignoring that and using our rule:
  $$=f(\sqrt{3},0)-f(0,1)=(\sqrt{3})^2-(1)^3=2$$
- ### Example 11.4.E1
  Calculate the area bounded by the astroidal ellipse, which is enclosed by $$C(t)= \langle a\cos(t)^3, b\sin(t)^3\rangle$$, for $$0 \leq t \leq 2\pi$$.
  
  $$A =\frac{1}{2}\oint^\uarr xdy - ydx$$
  $$=\frac{1}{2}\int_0^{2\pi} (a\cos^3(t))(3b\sin^2(t)\cos(t)dt-\frac{1}{2}\int_0^{2\pi}(b\sin^3(t)(3a\cos^2(t))(-\sin(t))dt$$
  $$\text{or}$$
  $$=\frac{3ab}{8}\int_0^{2\pi}\frac{1-\cos(4t)}{2}dt$$
  $$\text{or}$$
  $$=\frac{3\pi ab}{8}$$
  
  *(he might have gotten this one wrong, use other examples!!)*
- ### Example 11.4.E2
  Evaluate $$I = \oint^\uarr x^2ydx+x^4dy$$ for $$C$$ the boundary of the rectangle with vertices $$(0,0,(1,0),(1,4),(0,4)$$, traversed with positive orientation in this order.
  
  We can use ((66324325-c13a-47b6-92fe-4e5215b7077b)) to reduce this to a double integral.
  $$I = \int\int_D(\frac{dQ}{dx} - \frac{dP}{dy})dA$$
  $$\text{or}$$
  $$=\int_0^1\int_0^4(4x^3-x^2)dydx$$
  $$\text{or}$$
  $$=\int_0^4dy\int_0^1(4x^3 - x^2)dx$$
  $$\text{or}$$
  $$=\frac{8}{3}$$
- ### Example 11.4.E3
  Suppose that $$C$$ is a simple piecewise smooth curve, and let $$D$$ denote then interior of the positevly oriented curve. Show that the integral...
  $$\oint^\uarr_C\frac{-ydx+xdy}{x^2+y^2}$$
  ...is zero if $$D$$ does not contain the origin $$(0,0)$$ and is $$2\pi$$ if it does.
  
  We'll apply ((66324325-c13a-47b6-92fe-4e5215b7077b)).
  
  **For a region that doesn't include (0,0)**:
  $$=\frac{y^2-x^2}{(x^2+y^2)^2}-\frac{y^2-x^2}{(x^2+y^2)^2}$$
  
  **For a region that *does* include (0,0)**:
  $$=\int\int_{D_\rho}(\frac{dQ}{dx}+\frac{dP}{dy})dA + (\int\int_{D_2}(\frac{dQ}{dx}+\frac{dP}{dy})dA = 0)$$
  $$\text{so}$$
  $$=\lim_{\rho \rarr 0^{+}}\oint^\uarr\frac{-ydx + xdy}{x^2+y^2}dA = \lim_{\rho \rarr 0^{+}}\int\int_{D_\rho}\int_0^{2\pi}\frac{-\rho\sin(t)(-\rho\sin(t)dt+\rho\cos(t)(\rho\cos(t)dt}{(\rho\cos(t))^2+(\rho\sin(t))^2}$$
  $$\text{or}$$
  $$=\lim_{\rho \rarr 0^{+}}\int_0^{2\pi}(\frac{\rho^2}{\rho^2})(\frac{\sin^2(t)\cos^2(t)}{\sin^2(t)\cos^2(t)})dt$$
  $$\text{or}$$
  $$=\lim_{\rho \rarr 0^{+}}\int_0^{2\pi}dt$$
  $$\text{or}$$
  $$=2\pi$$