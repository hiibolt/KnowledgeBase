## Definition
Extrema occur where the gradients of a boundary curve and some level curves are equal.

For a given extrema subject to the constraint $g(x,y) = 0$ at $(x_0, y_0)$, we can parameterize $g=0$ as $\gamma(t) = (x(t), y(t))$.
Allowing $h(t) = f(\gamma(t)) = f(x(t), y(t))$ - $h(t) = 0, h'(t_0) = 0$ when $\gamma(t_0) = (x_0, y_0)$ gives us:
$$0=\frac{df}{dx}\frac{dx}{dt}+\frac{df}{dy}\frac{dy}{dt}$$

In other words, the gradient of f is orthogonal to the velocity vector $\gamma '(t_0)$, as is $\nabla g$.
	- ## 6.1 - Lagrange Multplier:
	  There is a number $\lambda$ allowing $\nabla f(x_0, y_0) = \lambda\nabla g(x_0,y_0)$
		- ### 6.1.E1
		  Find the extrema of $f(x,y) = 4xy$ subject to constraint $4x^2+9y^2=36$
		  
		  $\lambda f = <4y, 4x> z\lambda g = z<8x, 18y>$
		  \begin{cases}
		  4y = 8zx\\
		  4x=18zy\\
		  4x^2+9y^2=36
		  \end{cases}
		  $$\text{or}$$
		  $$z=\frac{y}{2x} = \frac{2x}{9y}$$
		  $$\text{so}$$
		  $$x^2=\frac{9}{4}y^2$$
		  $$\text{substituting...}$$
		  $$y^2 = 2 \text{ or }y=\pm\sqrt{2}$$
		  $$x=\pm\frac{3}{\sqrt{2}}$$
		  Therefore, our points are:
		  * $(\frac{3}{\sqrt{2}},\sqrt{2})$
		  * $(\frac{3}{\sqrt{2}},-\sqrt{2})$
		  * $(\frac{-3}{\sqrt{2}},\sqrt{2})$
		  * $(\frac{-3}{\sqrt{2}},-\sqrt{2})$
		- ### 6.1.E2