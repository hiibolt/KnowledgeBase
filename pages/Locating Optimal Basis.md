## Proposed Replacement for the $1,x,x^2$ basis
By minimizing $a+bx+cx^2$ against $x^3$, we get $\left\lbrace1,\sqrt3(1-2x),\sqrt5(1-6x+6x^2)\right\rbrace$.

To find the new $a,b,\text{ and }c$ for $x^3$ over $\left\lbrack0,1\right\rbrack$ in this new basis, take the dot product of each basis vector and add them together multiplied by each of those basis vector.

For example:
$$f(x)=(\int_0^1{(x^3)(1)}dx)(1)+(\int_0^1(x^3)(\sqrt{3}(1-2x))dx)(\sqrt{3}(1-2x))+(\int_0^1{(x^3)(\sqrt5(1-6x+6x^2))}dx)\sqrt5(1-6x+6x^2)$$
$$\text{or}$$
$$f(x)=\frac{1}{20}(1-12x+30x^2)$$
- ## Maximizing $f\left(x,y\right)=x+2y$ subject to $x^2+y^2=1$
  First, let's find our **Lagrangian equation**:
  $$L(x,y,\lambda)=(x+2y)-\lambda(x^2+y^2-1)$$
  
  Next, let's take the partial derivatives:
  $$\frac{\partial L}{\partial x}=1-2\lambda x=0$$
  $$\frac{\partial L}{\partial y}=2-2\lambda x=0$$
  
  So, the system we must solve is:
  \begin{cases}
  x = \frac{1}{2\lambda} \\
  y = \frac{1}{\lambda} \\
  x^2 + y^2 = 1
  \end{cases}
  $$(\frac{1}{2\lambda})^2+(\frac{1}{\lambda})^2=1$$
  $$\text{or}$$
  $$\lambda=\frac{\sqrt3}{2}$$
  
  Now that we have our $\lambda$ value:
  \begin{cases}
  x = \frac{1}{2\frac{\sqrt{3}}{2}} = \frac{1}{\sqrt{5}}
  y = \frac{1}{\frac{\sqrt{3}}{2}} = \frac{2}{\sqrt{5}}
  \end{cases}