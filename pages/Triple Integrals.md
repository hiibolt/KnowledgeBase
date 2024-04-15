## Definition
Becomes generalized to have bounds $[a,b] \times [c,d] \times [e,f]$.

$$\int\int\int_B(f(x,y,z))dV=\lim_{l,m,n\rarr\infty}\sum_{i=1}^l\sum_{j=1}^m\sum_{k=1}^nf(x_{ijk}^{*},y_{ijk}^{*},z_{ijk}^{*})\Delta x_i\Delta y_j \Delta z_k$$

Thankfully, this can be treated instead as a triple iterated integral in any of the 6 possible orders of integration.

**Example Setup**:
Set up the triple integral $$\int\int\int_B(x^2+y^2+z^2)dv\text{ for }B = [0,1]\times[0,2]\times[0,3]$$

$$\int_0^1\int_0^2\int_0^3(x^2+y^2+z^2)dzdydx$$
	- ### Example 8.1.E1
	  Evaluate the integral $$\int\int\int_Bx^2\sqrt{y}z^3dV$$ for $$B = [-1,3]\times[2,4]\times[1,5]$$.
	  
	  (Use above theorem!)
	- ### Example 8.1.E2
	  Evaluate $${\int\int\int}_E(x^2)dV$$ where $E$ is the region bounded by the graph of $$.
	  
	  $$\int_{-1}^1\int_{y^2}^1\int_0^{1-x^2}(x^2)dzdxdy$$
	- ### Example 8.1.E3
	  Express for the region bounded by the graph so f the plane $y=1-x$ and the cylinder $z = 1-x^2$ as a triple iterated integral.
	  $$D = \{(x,y) | 0 \leq x \leq 1, 0 \leq y \leq 1-x \}$$
	  $$E=\{ (x,y,z) | E, 0 \leq z \leq z = 1 - x^2 \}$$
	  $$\int_0^1\int_0^{1-x}\int_0^{1-x^2}(f(x,y,z))dzdydx$$
- ## Cylindrical Coordinates
  $$E=\{(x,y,z) | (x,y) \in D, u_1(x,y) \leq x \leq u_2(x,y)\}$$
  $$D=\{(r,\theta) | \alpha \leq \theta \leq \beta, h_1(\theta) \leq r \leq h_2(\theta)\}$$
  $$\int_\alpha^\beta\int_{h_1(\theta)}^{h_2(\theta)}(g(r\cos\theta,r\sin\theta)r)drd\theta$$
	- ### Example 8.2.E1
	  Find the volume bounded by the parabola $z = x^2 + y^2$ over the circle of radius 1 centered at $(1,0)$, *with the region plotted below*.
	  
	  $$\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\int_0^{2\cos\theta}\int_0^{r^2}(r)dzdrd\theta$$
	  $$\int_{-\frac{\pi}{2}}^{\frac{\pi}{2}}\int_0^{2\cos\theta}(r^3)drd\theta$$
	- ### Example 8.2.E2
	  Evaluate $$\int\int\int_E((x^2+y^2)^3)dv$$, for $E$ bounded by $z = 1-x^2-y^2$ and $z \geq 0$.
	  
	  $$\int_0^{2\pi}\int_0^{1}\int_0^{1-r^2}(r^7)dzdrd\theta$$
- ## Spherical Coordinates
  For points on spheres $x^2+y^2+z^2=\rho^2$, for $\rho > 0$, there are two angles that uniquely identify it.
  
  $\phi$ is measured from the $z$-axis down.
  $$x=\rho\sin\phi\cos\theta$$
  $$y=\rho\sin\phi\sin\theta$$
  $$z=\rho\cos\phi$$
	- ### Example 8.3.E1
	  Convert the Cartesian point $(x,y,z) = (\frac{1}{\sqrt{2}},-\sqrt{\frac{3}{2}},\sqrt{2})$ to spherical coordinates.
	  
	  $\rho = \sqrt{\frac{1}{\sqrt{2}}^2+(-\sqrt{\frac{3}{2}})^2+(\sqrt{2})^2} = 2$
	  $\phi = \cos^{-1}(\frac{\sqrt{2}}{2})=\frac{\pi}{4}$
	  $\theta = \cos^{-1}(\frac{\frac{1}{\sqrt{2}}}{2\sin(\frac{\pi}{4})})=\frac{\pi}{3}$
	- ### Example 8.3.E2
	  Convert the spherical point $(\rho,\theta,\phi) = (2,\frac{\pi}{3},-\frac{\pi}{6})$.
	  $$x=2\sin(-\frac{\pi}{6})\cos(\frac{\pi}{3})$$
	  $$y=2\sin(-\frac{\pi}{6})\sin(\frac{\pi}{3})$$
	  $$z=2\cos(-\frac{\pi}{6})\cos(\frac{\pi}{3})$$