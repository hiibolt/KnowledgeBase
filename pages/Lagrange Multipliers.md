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
		  Find the extrema of $f(x,y) = 4x^2+9y^2$ subject to constraint $x^2+y^2=1$
		  
		  $\nabla f = <8x, 18y>$
		  $\delta\nabla g = <2x, 2y>$
		  
		  Now:
		  \begin{cases}
		  8x=2\delta x\\
		  18y=2\delta y\\
		  x^2+y^2=1
		  \end{cases}
		  Since cancelling $x$ or $y$ in either case yields varying \delta values, either $x = 0$ or $y = 0$.
		  
		  ...
		  
		  $\therefore (1,0), (0,1), (-1,0), (0,-1)$
		- ### 6.1.E3
		  Find extrema of $f(x,y) = 3x + 4y$ subject to constraint $x^2 + y^2 \leq 25$
		  *Reminder - Solutions never occur on the interior.*
		  
		  $$\nabla f = <3, 4>$$
		  $$\delta\nabla g = \delta<2x, 2y>$$
		  Now:
		  \begin{cases}
		  3 = \delta 2x\\
		  4= \delta 2y\\
		  x^2 + y^2 = 25
		  \end{cases}
		  So:
		  $$\frac{3}{2x}=\frac{2}{y} \text{ >>> or >>> }\frac{4}{3}x=y$$
		  $\therefore (3, 4), (-3, -4)$
		- ### 6.1.E4
		  Find the extrema of $f(x,y,z) = x + y +z$ subject to the constraint $x^2+4y^2+9z^2=36$
		  
		  $$\nabla f = <1, 1, 1>$$
		  $$\delta\nabla g = \delta<2x, 8y, 18z>$$
		  Now:
		  \begin{cases}
		  \delta(2x) = 1\\
		  \delta(8y) = 1\\
		  \delta(18z) = 1\\
		  x^2 + 4y^2 + 9z^2 = 36
		  \end{cases}
		  So:
		  $$x = 4y$$
		  $$z = \frac{4}{9}y$$
		- #### 6.1.E5
		  Maximize the volume of a rectangular box, symmetric about the $xy$, $xz$, and $yz$ planes, and inscribed in a general ellipsoid $\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1$.
		  
		  Because this box is symmetric, $\frac{x^2}{a^2} + \frac{y^2}{a^2} + \frac{z^2}{a^2} = 1$
		  
		  $V=8xyz$, subject to $g(x,y,z) = \frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} - 1$
		  $\nabla f = <8yz, 8xz, 8xy>$
		  $\delta\nabla g = \delta<\frac{2x}{a^2},\frac{2y}{b^2},\frac{2z}{c^2}>$
		  $$8yz=\frac{2x}{a^2}, 8xz=\frac{2x}{a^2}$$
-