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
  Find the work done by Newton's gravitational field, which we defined as the vector field $$F(x,y,z) = -\frac{mMg}{(x^2+y^2+z^2)^\frac{3}{2}}<x,y,z>$$ in moving an object from the point $$P$$