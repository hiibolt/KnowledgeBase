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