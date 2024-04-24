## Definition
$$\int_C f(x,y) dx = \lim_{n\rarr\infty}\sum_{i=1}^{n}f(x(t^{*}),y(t^{*}))\Delta x_i$$

For a line integral for space curve $C$ with $$a\leq t \leq b$$,
$$\int_Cf(x,y,z) = \int_a^b(f(x(t),y(t),z(t))x'(t))dt$$
$$\int_Cf(x,y,z) = \int_a^b(f(x(t),y(t),z(t))y'(t))dt$$
$$\int_Cf(x,y,z) = \int_a^b(f(x(t),y(t),z(t))z'(t))dt$$

When inte
- ## Example 11.1.E1
  Evaluate $$\int_C P(x,y)dx, \int_C Q(x,y)dy$$ and $$\int_C(P(x,y) + Q(x,y))dy$$ for $$P(x,y) = x+2y$$ and $$Q(x,y) = 2x^2 - 5xy$$ for $$C(t) = (t,t^2)$$ with $$0\leq t\leq 1$$
  
  $$\int_CPdx = \int_0^1(t+2t^2)(1)dt=\frac{7}{6}$$
  $$\int_CQdy = \int_0^1((2t^2-5t(t^2))(2t))dt=-1$$
  $$\text{so}$$
  $$\int_C(Pdx+Qdy) = \frac{7}{6}-1 = \frac{1}{6}$$