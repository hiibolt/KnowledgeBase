### Refreshers
	- #### Spaces of Numbers
	  
	  $$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \R \subset \mathbb{C}$$
		- #### Notable Operations
		  * $+$ and $*$ work fine in all spaces.
		  * $-$ does not always work in $\N$
		  * $/$ does not work when dividing by zero
		- #### Notable Facts
		  A **field** (Q, $\R$, and $C$) guarantee a conjugate of every set element.
		- #### E1. Example Equation
		  $$ax=b$$
		  
		  In this case, $ax$ is a **linear expression** in $x$.
			- #### Distributive Law
			  Consider that by the distributive law, this could also be $a\left(x+x^{^{\prime}}\right)$, or, $ax+ax^{^{\prime}}$.
			  
			  This **linear expression** can be notated as $L:\mathbb{R}\to\mathbb{R}$.
			  
			  $$L_{a}\left(x\right)=ax$$
			  $$L_{a}\left(x+x^{^{\prime}}\right)=L_{a}\left(x\right)+L_{a}\left(x^{^{\prime}}\right)$$
			- #### Multiplicity
			  $$a\left(x\cdot x^{^{\prime}}\right)=\left(ax\right)x^{^{\prime}}=x\left(ax^{^{\prime}}\right)$$
			  $$\text{or...}$$
			  $$L_{a}\left(x\cdot x^{\prime}\right)=xL_{a}\left(x^{\prime}\right)$$
			  $L$ *is still linear! On top of this, these are the only linear maps.*
		- #### E2. Two-Dimensional
		  We will swap $\mathbb{R}$ for $\mathbb{R}^2$, at least somewhere!
		  
		  **Options**:
		  * Parameterized curve in the plane
		  $$L_{I}:\mathbb{R}\to\mathbb{R}^2$$
		  $$L_{I}\left(x\right)=\left(ax,a^{\prime}x\right)$$
		  $$\text{or}$$
		  $$=\left(a,a^{\prime}\right)x$$
		  * Scalar Field
		  $$L_{II}:\R^2->\R$$
		  $$L_{II}\left(x,x^{\prime}\right)=ax+a^{\prime}x^{\prime}$$
		  * Vector Field
		  $$L_{III}:\R^2->\R^2$$
		  $$L_{III}\left(x,x^{\prime}\right)=\left(ax+bx^{\prime},cx+\mathrm{d}x^{\prime}\right)$$
		  *Again, these are the only linear maps.*
- ## Gaussian Elimination 
  \begin{equation}
  \begin{bmatrix}
  a & b \\
  c & d
  \end{bmatrix}
  \begin{bmatrix}
  x_1 \\
  x_2
  \end{bmatrix}
  =
  \begin{bmatrix}
  e \\
  f
  \end{bmatrix}
  \end{equation}
	- #### E1. Example Problem
	  \begin{cases}
	  y=4 \\
	  2x+3y=5
	  \end{cases}
	  
	  \begin{equation}
	  \begin{bmatrix}
	  0 && 1 \\
	  2 && 3
	  \end{bmatrix}
	  \begin{bmatrix}
	  x \\
	  y
	  \end{bmatrix}
	  =
	  \begin{bmatrix}
	  4 \\
	  5
	  \end{bmatrix}
	  \end{equation}
	  
	  **Solving**:
	  We know that $y=4$, so then we can do the following:
	  $$2x+3\cdot4=5$$
	  $$\text{or}$$
	  $$x=\frac{-7}{2}$$
	- #### E2. Example Problem (Continues 1)
	  \begin{equation}
	  \begin{bmatrix}
	  \not{0} && 1 \\
	  2 && 3
	  \end{bmatrix}
	  |
	  \begin{bmatrix}
	  4 \\
	  5
	  \end{bmatrix}
	  \end{equation}
	  
	  $$\text{swapping}$$
	  
	  \begin{equation}
	  \begin{bmatrix}
	  2 && 3\\
	  \not{0} && 1
	  \end{bmatrix}
	  |
	  \begin{bmatrix}
	  5 \\
	  4
	  \end{bmatrix}
	  \end{equation}
	  
	  $$\text{or}$$
	  
	  \begin{equation}
	  \begin{bmatrix}
	  1 && 3/2\\
	  \not{0} && 1
	  \end{bmatrix}
	  |
	  \begin{bmatrix}
	  5/2 \\
	  4
	  \end{bmatrix}
	  \end{equation}
	  
	  $$\text{or}$$
	  
	  \begin{equation}
	  \begin{bmatrix}
	  1 && 3/2\\
	  \not{0} && -3/2
	  \end{bmatrix}
	  |
	  \begin{bmatrix}
	  5/2 \\
	  -6
	  \end{bmatrix}
	  \end{equation}
	  
	  $$\text{or}$$
	  
	  \begin{equation}
	  \begin{bmatrix}
	  1 && 0\\
	  \not{0} && 1
	  \end{bmatrix}
	  |
	  \begin{bmatrix}
	  (5/2 - 6)\text{ or }\frac{-7}{2} \\
	  4
	  \end{bmatrix}
	  \end{equation}