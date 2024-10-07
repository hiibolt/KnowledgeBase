## Steps
The following example is for fitting $a+bx+c^2$ to $x^3$.

$$a,b,\text{ and }c$$ are assumed to be arbitrary constants we must find to minimize an error function.
	- ### Step 1 - Define
	  First, define the function measuring error based on a loss function:
	  $$E\left(a,b,c\right)=\sqrt{L\left(a,b,c\right)}$$
	  $$L\left(a,b,c\right)=\int_0^1\left(x^3-\left(a+bx+c^2\right)\right)^2dx$$
	- ### Step 2 - Expand
	  Second, expand the integrand:
	  $$\ldots\left(x^3-a-bx-c^2\right)^2\ldots$$
	- ### 3 - Gradient
	  Next, create the gradient of the new integral with respect to each $a,b,\text{ and }c$.
	  \begin{cases}
	  \frac{d}{da}L(a,b,c)
	  \frac{d}{}