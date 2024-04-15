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
	  
	  $$\int_0^{2\pi}\int_0^{2\cos\theta}\int_0^{r^2}r)dzdrd\theta$$