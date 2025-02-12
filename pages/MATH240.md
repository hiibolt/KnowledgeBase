### Linearity
id:: 67927673-4212-4c3a-b706-2c7c6c21abc9
For a function $$L$$, it must satisfy:
$$L(x+y)=L(x) + L(y)$$
$$L(cX) = cL(x)$$

For example, the derivative operation is linear:
$$\int(f+g) = \int{f} + \int{g}$$
$$\int(cf) = c\int{f}$$
- ### Sigma Notation
  $$\sum_{i=1}^3f(i)=f(1)+f(2)+f(3)$$
  $$\sum_{i=1}^3f(i)+g(i)=(f(1)+g(1))+(f(2)+g(2))+(f(3)+g(3))=\sum_{i=1}^3f(i)+\sum_{i=1}^3g(i)$$
  $$\sum_{i=3}^32f(i)=2f(1)+2f(2)+2f(3)=2\sum_{i=1}^3f(i)$$
  
  These properties prove that **Sigma Notation** has valid ((67927673-4212-4c3a-b706-2c7c6c21abc9)).
  
  $$\sum_{i=1}^3\sum_{j=1}^3f_j(i)=\sum_{j=1}^3\sum_{i=1}^3f_j(i)$$
- [[Matrice Definitions]]
- [[Matrice Operations]]
- [[Matrice Transformations]]
- [[Matrice Functions]]
- ### Matrices
	- #### Notation
	  A matrix of $n$ vertical size and $m$ horizontal size appears as:
	  \begin{vmatrix}
	  a_{11} & a_{12} & ... & a_{1m} \\
	  a_{21} & a_{22} & ... & a_{2m} \\
	  ... & ... & ... & ... \\
	  a_{n1} & a_{n2} & ... & a_{nm} \\
	  \end{vmatrix}
	  
	  Notationally, this is described as $$M_{n,m}(\mathbb{R})$$.
	  
	  A vector can be distinguished from a standard matrix by the arrow over the variable.
	  
	  For example: $$v \text{ vs. } \vec{v}$$.
	  
	  A **position vector** is found by placing a vector to act on the origin.
	- #### Visualization
	  Action of column vectors...
	  \begin{vmatrix}x \\ y \end{vmatrix}
	  ...on $$\mathbb{R}^2$$.
	  
	  \begin{equation}
	  \begin{vmatrix}2 \\ 1 \end{vmatrix}
	  ...moves...
	  \begin{vmatrix}1 \\ 0\end{vmatrix}
	  ...to...
	  \begin{vmatrix}3 \\ 1\end{vmatrix}
	  \end{equation}
	- ### Functions
	  A function $f : S \rarr T$ is a set of ordered pairs $(s,t)$ where $s\in S$ and $t \in T$, such that for every $s \in S$, there exists exactly one $t\in T$ for which $f(x)=t$.
	  
	  $S$ can be defined as the *domain*
	  $T$ can be defined as the *codomain*, **not** to be confused with the term *range*.
		- ### Linear Functions
		  $$f : \mathbb{R}^n \rarr \mathbb{R}m$$
		  $$\vec{v} \mapsto A\vec{v}$$
		  It's worth noting that the above notation is *maps-to* notation, which can be re-written as:
		  $$f(\vec{v})=A\vec{v}$$
		  
		  Requirements to be a linear function:
		  $$f(\vec{v}_1+\vec{v}_2)=f(\vec{v}_1)+f(\vec{v}_2)$$
		  $$f(c\vec{v})=cf(\vec{v})$$
		- ### Composition
		  Let $f:A\rarr B$ be a function and $g:B\rarr C$ be another function.
		  
		  The composition of *f and g* is the function:
		  $(g\circ f)(x)=g(f(x))$ where $g\circ f:A\rarr C$
		  
		  This is read as "$g$ composed with $f$". This composition is *only* valid if the *image* of $f$ is contained in the domain of $g$.
- ### Fields
  **Examples**:
  * Scalars
    * $\mathbb{Q}$ - The field of rational numbers
    * $\mathbb{R}$ - Real numbers
  * Complex
    * $\mathbb{C}$ - Complex numbers ($$\{x+iy : x,y \in \mathbb{R}, i^2=-1\}$$)
- _unorganized
	- #### Law of Cosines
	  id:: 67893c87-26ba-4786-9c07-c8155c2f7015
	  For a triangle with sides $a$ and $b$ with angle $\theta$:
	  $$c^2 = a^2+b^2-2ab\cos{\theta}$$
- #### old
  collapsed:: true
	- ### Refreshers
	  collapsed:: true
		- #### Spaces of Numbers
		  
		  $$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \R \subset \mathbb{C}$$
			- #### Notable Operations
			  * $+$ and $*$ work fine in all spaces.
			  * $-$ does not always work in $\N$
			  * $/$ does not work when dividing by zero
			- #### Notable Facts
			  A **field** (Q, $\R$, and $C$) guarantee a conjugate of every set element.
		-
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
			- ### Parameterized curve in the plane
			  $$L_{I}:\mathbb{R}\to\mathbb{R}^2$$
			  $$L_{I}\left(x\right)=\left(ax,a^{\prime}x\right)$$
			  $$\text{or}$$
			  $$=\left(a,a^{\prime}\right)x$$
			  
			  \begin{cases}
			  a_1x = a \\
			  a_2x = b
			  \end{cases}
			  
			  $$\text{or}$$
			  \begin{equation}
			  \begin{bmatrix}
			  a_1 \\
			  a_2
			  \end{bmatrix} = \begin{bmatrix}
			  a \\
			  b
			  \end{bmatrix}
			  \end{equation}
			  
			  $$\text{or}$$
			  \begin{equation}
			  \begin{bmatrix}
			  1 \\
			  0
			  \end{bmatrix} = \begin{bmatrix}
			  a \\
			  b - \frac{a_2a}{a_1}
			  \end{bmatrix}
			  \end{equation}
			  
			  $$\text{so}$$
			  \begin{cases}
			  x = \frac{a}{a_1} \\
			  \frac{a_2a}{a_1} = b
			  \end{cases}
			- ### Scalar Field
			  $$L_{II}:\R^2->\R$$
			  $$L_{II}\left(x,x^{\prime}\right)=ax+a^{\prime}x^{\prime}$$
			  $$a_1x_1+a_2b_2=a$$
			  
			  $$\text{or}$$
			  \begin{equation}
			  \begin{bmatrix}
			  a_1 & a_2 
			  \end{bmatrix} = \begin{bmatrix}
			  a
			  \end{bmatrix}
			  \end{equation}
			  
			  $$\text{or}$$
			  \begin{equation}
			  \begin{bmatrix}
			  1 & \frac{a_2}{a_1} 
			  \end{bmatrix} = \begin{bmatrix}
			  \frac{a}{a_1}
			  \end{bmatrix}
			  \end{equation}
			  
			  $$\text{or}$$
			  $$x_1+\frac{a_2}{a_1}x_2=\frac{a}{a_1}$$
			- ### Vector Field
			  $$L_{III}:\R^2->\R^2$$
			  $$L_{III}\left(x,x^{\prime}\right)=\left(ax+bx^{\prime},cx+\mathrm{d}x^{\prime}\right)$$
			  *Again, these are the only linear maps.*
	- ## Gaussian Elim
	  collapsed:: true
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
		- ### E3. Example Problem
		  \begin{cases}
		  x + y + z = 3 \\
		  x - y + z = 2 \\
		  x - y - z = \alpha
		  \end{cases}
		  
		  $$\text{so}$$
		  
		  \begin{equation}
		  \begin{bmatrix}
		  1 & 1 & 1 \\
		  1 & -1 & 1 \\
		  1 & -1 & -1
		  \end{bmatrix}
		  |
		  \begin{bmatrix}
		  3 \\
		  2 \\
		  \alpha
		  \end{bmatrix}
		  \end{equation}
		  
		  $$\text{or}$$
		  
		  \begin{equation}
		  \begin{bmatrix}
		  1 & 0 & 0 \\
		  0 & 1 & 0 \\
		  0 & 0 & 1
		  \end{bmatrix}
		  |
		  \begin{bmatrix}
		  \frac{3 + \alpha}{2}  \\
		  \frac{1}{2} \\
		  \frac{2 - \alpha}{2}
		  \end{bmatrix}
		  \end{equation}
		  
		  $$\text{so}$$
		  
		  \begin{cases}
		  x = \frac{3}{2} + \frac{\alpha}{2} \\
		  y = \frac{1}{2} \\
		  z = \frac{2 - \alpha}{2}
		  \end{cases}
		  
		  One can verify this claim by choosing an arbitrary value for $\alpha$ to plug in. Likely, it's easiest to use $\alpha = 0$.
		  
		  We must also verify without choosing a value, however:
		  \begin{cases}
		  \frac{3}{2} + \frac{\alpha}{2} + \frac{1}{2} + 1 - \frac{\alpha}{2} = 3 \\
		  \frac{3}{2} + \frac{\alpha}{2} - \frac{1}{2} + 1 - \frac{\alpha}{2} = 2 \\
		  \frac{3}{2} + \frac{\alpha}{2} - \frac{1}{2} - 1 - \frac{\alpha}{2} = a
		  \end{cases}
		- ## Inconsistencies in GE
			- #### E1. Example Problem
			  \begin{cases}
			  x + 2y  + 6z = 5 \\
			  -x + y - 2z = 3 \\
			  x - 4y - 2z = 1
			  \end{cases}
			  
			  \begin{equation}
			  \begin{bmatrix}
			  1 & 2 & 6 \\
			  -1 & 1 & -2 \\
			  1 & -4 & -2 
			  \end{bmatrix} = \begin{bmatrix}
			  5 \\
			  3 \\
			  1
			  \end{bmatrix}
			  \end{equation}
			  
			  $$\text{or}$$
			  \begin{equation}
			  \begin{bmatrix}
			  1 & 2 & 6 \\
			  0 & 3 & 4 \\
			  0 & -6 & -8 
			  \end{bmatrix} = \begin{bmatrix}
			  5 \\
			  8 \\
			  -4
			  \end{bmatrix}
			  \end{equation}
			  
			  $$\text{or}$$
			  \begin{equation}
			  \begin{bmatrix}
			  1 & 2 & 6 \\
			  0 & 1 & \frac{4}{3} \\
			  0 & 0 & 0 
			  \end{bmatrix} = \begin{bmatrix}
			  5 \\
			  \frac{8}{3} \\
			  12
			  \end{bmatrix}
			  \end{equation}
			  
			  Notice that we currently have an inconsistency. Equation 3 can be interpreted literally as:
			  $$0x+0y+0z=12$$
			  
			  Which is a fundamentally incorrect equation. 
			  
			  **Because this *one* equation is inconsistent, the *entire* system is inconsistent, and the set of solutions is *empty*.**
			  
			  Had that $12$ been $0$, the equation would have been **redundant**.
			- ### E2. Example Problem
			  \begin{cases}
			  3x - 2y + 3z = 8 \\
			  x + 3y + 6z = -3 \\
			  2x + 6y + 12z = -6
			  \end{cases}
			  
			  \begin{equation}
			  \begin{bmatrix}
			  3 & -2 & 3 \\
			  1 & 3 & 6 \\
			  2 & 6 & 12 
			  \end{bmatrix} = \begin{bmatrix}
			  8 \\
			  -3 \\
			  -6
			  \end{bmatrix}
			  \end{equation}
			  
			  $$\text{or}$$
			  \begin{equation}
			  \begin{bmatrix}
			  1 & 3 & 6 \\
			  0 & -11 & -15 \\
			  0 & 0 & 0 
			  \end{bmatrix} = \begin{bmatrix}
			  -3 \\
			  17 \\
			  0
			  \end{bmatrix}
			  \end{equation}
			  
			  While this is **redundant**, we do carry on!
			  
			  $$\text{or}$$
			  \begin{equation}
			  \begin{bmatrix}
			  1 & 0 & \frac{21}{11} \\
			  0 & 1 & \frac{15}{11} \\
			  0 & 0 & 0 
			  \end{bmatrix} = \begin{bmatrix}
			  \frac{18}{11} \\
			  \frac{-17}{11} \\
			  0
			  \end{bmatrix}
			  \end{equation}
			  
			  $$\text{so}$$
			  \begin{cases}
			  x + \frac{21}{11}z = \frac{18}{11}\\
			  y + \frac{15}{11}z = \frac{-17}{11}
			  \end{cases}
			  
			  $$\text{or}$$
			  \begin{cases}
			  x = \frac{18}{11} - \frac{21}{11}z \\
			  y = \frac{-17}{11} - \frac{15}{11}z
			  \end{cases}
			  
			  In this case, the solutions for $x$ and $y$ are determined by $z$. Therefore, there is an **uncountable** number of solutions in solution set $S$ because $z$ can be any real number $\in\mathbb{R}$.
				- ### E2.1 - Example Problem (cont.)
				  Let $\alpha$ be a real number. (Set $z = \alpha$)
				  
				  \begin{equation}
				  =
				  \frac{18}{11}-\frac{21}{11}\alpha
				  \begin{bmatrix}
				  1 \\
				  0 \\
				  0
				  \end{bmatrix}
				  +
				  (-\frac{17}{11} - \frac{15}{11}a)
				  \begin{bmatrix}
				  0 \\
				  1 \\
				  0
				  \end{bmatrix}
				  +
				  a 
				  \begin{bmatrix}
				  0 \\
				  0 \\
				  1
				  \end{bmatrix}
				  \end{equation}
				  
				  $$\text{or}$$
				  \begin{equation}
				  =
				  \begin{bmatrix}
				  \frac{18}{11} \\
				  \frac{-17}{11} \\
				  0
				  \end{bmatrix} + 
				  \alpha
				  \begin{bmatrix}
				  \frac{-21}{11} \\
				  \frac{-15}{11} \\
				  1
				  \end{bmatrix}
				  \end{equation}
				  
				  This describes our set of solutions $S$ from our example in proper notation.
	- [[R Notation]]
	- [[Matrices]]
	- [[Proving Linearity]]
	- [[N-Dimensional Determinants]]
	- [[List Operations]]
	- **REVIEW THUS FAR**: [[Review 1]]
	- [[Vector Spaces]]
	- [[Minimizing Polynomial Estimation]]
	- [[Locating Optimal Basis]]
	- [[Maps Between Spaces of Differing Basis]]