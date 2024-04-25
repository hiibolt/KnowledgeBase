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

$$W=\int_CF\cdot Tds$$
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
-