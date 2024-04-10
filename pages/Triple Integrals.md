## Definition
Becomes generalized to have bounds $[a,b] \times [c,d] \times [e,f]$.

$$\int\int\int_B(f(x,y,z))dV=\lim_{l,m,n\rarr\infty}\sum_{i=1}^l\sum_{j=1}^m\sum_{k=1}^nf(x_{ijk}^{*},y_{ijk}^{*},z_{ijk}^{*})\Delta x_i\Delta y_j \Delta z_k$$

Thankfully, this can be treated instead as a triple iterated integral in any of the 6 possible orders of integration.

**Example Setup**:
Set up the triple integral $$\int\int\int_B(x^2+y^2+z^2)dv\text{ for }B = [0,1]\times[0,2]\times[0,3]$$

$$\int_0^1\int_0^2\int_0^3(x^2+y^2+z^2)dzdydx$$