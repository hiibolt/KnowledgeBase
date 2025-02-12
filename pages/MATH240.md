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
- ### Matrices
	- ### Definitions
		- #### Column Vector
		  A vertical set.
		  
		  For example, for the set of column vectors with elements of $$\mathbb{R}$$ is $$\mathbb{R}^{n}$$.
		- #### Row Vector
		  A horizontal set.
		  
		  For example, for the set of row vectors with elements of $$\mathbb{R}$$ is $$\mathbb{R}_{n}$$.
		- #### Diagonal Matrix
		  A matrix where all elements $m_{ij} = 0\text{ when }i\ne j$.
			- #### Scalar Diagonal Matrix
			  A diagonal matrix, but all elements are the same number.
			- #### Identity Matrix
			  A diagonal matrix, but all non-zero elements are 1.
		- ### Symmetric Matrix
		  A matrix where $A=A^T$
			- ### Skew Symmetric Matrix
			  A matrix where $A^T= -A$.
		- ### Nonsingular/Invertible Matrix
		  id:: 67a25d50-5203-40c8-a7c3-f3e65c7e765d
		  A matrix $A$ where there exists a matrix $B$ such that $AB = I_n$.
		  
		  This matrix $B$ is also called the *inverse* of $A$.
		- ### Singular/Noninvertible Matrix
		  id:: 67a25d50-6c70-43fd-bfae-9e0e7ebcd07e
		  A matrix $A$ where there exists *no* matrix $B$ such that $AB=I_n$.
		- ### Triangle Matrix
		  id:: 67a6470d-b340-4c59-b950-7d56e59bb513
		  A matrix $A$ where all elements above or below the diagonal are $0$.
		- ### Zero Vector
		  id:: 67912a9e-2bd7-4de0-ae70-fea77995ff98
		  $$\vec{0}\in\mathbb{R}^n$$
		  $$\vec{0}\in\mathbb{R}_m$$
		  Both are column/row vectors respectively with all elements set to 0.
		- #### Homogeneous
		  An equation $A\vec{x} = \vec{0}$ is called a *homogeneous* equation.
		- #### Inhomogeneous
		  An equation $A\vec{x} = \vec{b}$, where $\vec{b} \ne \vec{0}$, is called an *inhomogeneous* equation.
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
	- #### Operations
		- #### Scalar Multiplication
		  IF $$c \in \mathbb{R}$$, then 
		  \begin{equation}
		  c
		  \begin{bmatrix}
		  a_{11} & a_{12} & ... & a_{1m} \\
		  a_{21} & a_{22} & ... & a_{2m} \\
		  ... & ... & ... & ... \\
		  a_{n1} & a_{n2} & ... & a_{nm} \\
		  \end{bmatrix}=
		  \begin{bmatrix}
		  ca_{11} & ca_{12} & ... & ca_{1m} \\
		  ca_{21} & ca_{22} & ... & ca_{2m} \\
		  ... & ... & ... & ... \\
		  ca_{n1} & ca_{n2} & ... & ca_{nm} \\
		  \end{bmatrix}
		  \end{equation}
		- #### Addition
		  \begin{equation}
		  \begin{bmatrix}
		  a_{11} & a_{12} & ... & a_{1m} \\
		  a_{21} & a_{22} & ... & a_{2m} \\
		  ... & ... & ... & ... \\
		  a_{n1} & a_{n2} & ... & a_{nm} \\
		  \end{bmatrix}+
		  \begin{bmatrix}
		  b_{11} & b_{12} & ... & b_{1m} \\
		  b_{21} & b_{22} & ... & b_{2m} \\
		  ... & ... & ... & ... \\
		  b_{n1} & b_{n2} & ... & b_{nm} \\
		  \end{bmatrix} =
		  \begin{bmatrix}
		  a_{11} + b_{11} & a_{12} + b_{12} & ... & a_{1m} + b_{1m}\\
		  a_{21} + b_{21} & a_{22} + b_{22} & ... & a_{2m} + b_{2m} \\
		  ... & ... & ... & ... \\
		  a_{n1} + b_{n1} & a_{n2} + b_{n2} & ... & a_{nm} + b_{nm}\\
		  \end{bmatrix}
		  \end{equation}
		- #### Transpose
		  \begin{equation}
		  \begin{bmatrix}
		  a_{11} & ... & a_{1m} \\
		  ... & ... & ... \\
		  a_{n1} & ... & a_{nm}
		  \end{bmatrix}^T = 
		  \begin{bmatrix}
		  a_{11} & ... & a_{m1} \\
		  ... & ... & ... \\
		  a_{1n} & ... & a_{mn}
		  \end{bmatrix} 
		  \end{equation}
		- #### Vector Length
		  Denoted by $$||\vec{v}||$$.
		  
		  For example, in $$\mathbb{R}^2$$:
		  $$||\vec{v}|| = \sqrt{a^2 + b^2}$$
		  
		  In $$\mathbb{R}^3$$:
		  $$||\vec{v}|| = \sqrt{a^2 + b^2 + c^2}$$
		  
		  In $$\mathbb{R}^n$$:
		  $$||\vec{v}|| = \sqrt{a_1^2 + a_2^2 + ... + a_n^2}$$
		- #### Dot Product
		  id:: 6787f568-1935-41ae-a8f4-adcc0fe55c86
		  $$(a_1,...,a_n)^{(T)}\cdot (b_1,...,b_n)^{(T)}=a_1b_1+...+a_nb_n$$
		  $$\vec{x}\cdot\vec{y} = ||\vec{x}||||\vec{y}||\cos{\theta}$$
			- #### Cauchy-Schwarz
			  Guarantees that for any $\vec{x},\vec{y}\in\mathbb{R}^n$,
			  $$-1<\frac{\vec{x}\cdot\vec{y}}{||\vec{x}||||\vec{y}||}<1$$
			- #### Implications
			  Firstly, we must recall the ((67893c87-26ba-4786-9c07-c8155c2f7015)).
			  
			  By knowing this, we can use the dot product to find perpendicular vectors by solving.
			  
			  In general, this formula is represented for a $$\mathbb{R}^2$$ vector $$\vec{x}={a,b}$$, you should select a vector $$\vec{s} = {\pm b,\pm a}$$ where *one of* $a$ or $b$ is negative.
			  
			  The length of a vector squared is the same vector dot itself, giving the following:
				- ### Hypotenuse Theorem
				  $${||\vec{x}||}^2=\vec{x}\cdot\vec{x}$$
			- #### Special Properties
			  $$\vec{u}\cdot(\vec{v}+\vec{w})=a_1(b_1+c_1)+...+a_n(b_n+c_n)$$
			  $$\text{or}$$
			  $$=\vec{u}\cdot\vec{v}+\vec{u}\cdot\vec{w}$$
		- #### Projection
		  $$P_{\vec{v}}{\vec{u}}=\frac{\vec{u}\cdot\vec{v}}{\vec{v}\cdot\vec{v}}\vec{v}$$
		  
		  $P_{\vec{v}}\vec{u}$ is read as "projecting $\vec{u}$ onto $\vec{v}$.
		- ### Null Space
		  For a given matrix $A$, it is the solution set of $A\vec{x}=\vec{0}$
		- ### Matrix Multiplication
		  The general process is to go *down* the rows of the first (left) matrix and *across* the columns of the second (right) matrix, and take the ((6787f568-1935-41ae-a8f4-adcc0fe55c86)) of the two.
			- #### Algebraic Properties (of addition, technically)
			  Let $A$, $B$, and $C$ be $mxn$ matrices. Then,
			  $$A+B = B + A$$
			  $$A+(B+C)=(A+B)+C$$
			  $$\text{There exists a unique matrix }0_{mn}\text{ such that } A+0_{mn}=A$$
			  ...where $0_{mn}$ is a ((67912a9e-2bd7-4de0-ae70-fea77995ff98)).
			  $$A+(-A)=0$$
			  $$-A=(-1)*A$$
			- #### Properties
				- #### Property 1
				  $$A(BC)=(AB)C$$
				  ...is proven by:
				  
				  For $A_{mxn}$, $B_{nxp}$, and $pxq$:
				  $$BC=(\sum_{s=1}^pb_{js}c_{sk})$$
				  $$A(BC)=(\sum_{r=1}^na_{ir}\sum_{s=1}^pb_{rs}c_{sk})=\sum_{s=1}^p\sum_{r=1}^na_{ir}b_{rs}c_{sk}$$
				- #### Property 2/3
				  $$(A+B)C=AC+BC$$
				  $$C(A+B)=CA+CB$$
				  ...is proven by:
				  
				  For $A_{mxn}$, $B_{mxn}$, and $C_{nxp}$:
				  $$\sum_{r=1}^n(a_{ir}+b{ir}c_{rj})=....=AC+BC$$
			- #### Using Sigma Notation
			  $$c_{ij}=\sum_{\lambda=1}^n(a_{i\lambda}b_{i\lambda})$$
		- #### Determinant
		  In general, the pattern for determining the signs of a determinant matrix is:
		  \begin{bmatrix}
		  + & - & + & \dots \\
		  - & + & - & \dots \\
		  + & - & + & \dots \\
		  \dots & \dots & \dots & \dots
		  \end{bmatrix}
		  
		  * If a row or column of the matrix is 0, the determinant is also zero.
		  * The determinant is zero if and only for a ((67a25d50-6c70-43fd-bfae-9e0e7ebcd07e)).
		  * $|A|=|A^T|$
		  * $|AB|=|A||B|$
		  * $|I| = 1$
		  * If two rows or columns of $A$ are equal, then $|A| = 0$
		  * If you interchange two rows or columns, the determinant changes sign.
		  * If $B$ is the matrix obtained by multiplying a row or column of $A$ by a scalar $c\in \mathbb{R}$, then $|B| = c|A|$
		  * The determinant of an upper ((67a6470d-b340-4c59-b950-7d56e59bb513)) $A_{nxn}\text{ is }\sum_{i=1}^na_{ii}$.
		  * If you add a multiple of one row or column to another, the determinant is unchanged.
			- #### 2x2
			  \begin{equation}
			  \det
			  \begin{bmatrix}
			  a & b \\
			  c & d
			  \end{bmatrix}
			   = ad - bc
			  \end{equation}
			  
			  This has the special property where 
			  \begin{equation}
			  |\det\begin{bmatrix}u_1 & v_1 \\ u_2 & v_2\end{bmatrix}|
			  \end{equation} is the area of the parallelogram described by vertices $\vec{u}$ and $\vec{v}$.
			- #### 3x3 
			  \begin{equation}
			  \det
			  \begin{bmatrix}
			  a & b & c \\
			  d & e & f \\
			  g & h & i
			  \end{bmatrix} = 
			  a\begin{vmatrix} e & f \\ h & i\end{vmatrix}
			  -b\begin{vmatrix} d & f \\ g & i\end{vmatrix}
			  +c\begin{vmatrix} d & e \\ g & h\end{vmatrix}
			  \end{equation}
			  
			  **Example 1**:
			  \begin{equation}
			  \det
			  \begin{bmatrix}
			  2 & 0 & 1 \\
			  0 & 1 & 0 \\
			  2 & -1 & 4
			  \end{bmatrix}
			  =
			  6
			  \end{equation}
			  
			  **Example 2**:
			  \begin{equation}
			  \det
			  \begin{bmatrix}
			  2 & 1 & -1 \\
			  1 & 3 & 0 \\
			  0 & 2 & 1
			  \end{bmatrix}
			  =
			  3
			  \end{equation}
			- #### 4x4
			  \begin{equation}
			  \det
			  \begin{bmatrix}
			  a & b & c & d \\
			  e & f & g & h \\
			  i & j & k & l \\
			  m & n & o & p
			  \end{bmatrix}
			  =
			  a\det\begin{bmatrix}
			  f & g & h \\
			  j & k & l \\
			  m & n & o
			  \end{bmatrix}
			  -b\det\begin{bmatrix}
			  e & g & h \\
			  i & k & l \\
			  m & o & p
			  \end{bmatrix}
			  +c\det\begin{bmatrix}
			  e & f & h \\
			  i & j & l \\
			  m & n & p
			  \end{bmatrix}
			  -d\det\begin{bmatrix}
			  e & f & g \\
			  i & j & k \\
			  m & n & o
			  \end{bmatrix}
			  \end{equation}
		- #### Cross Product
		  $$A\times B = ||A||||B||\sin\theta$$
		  
		  The cross product of two vectors $\vec{u}_{2x1}$ and $\vec{v}_{2x1}$ is:
		  \begin{equation}
		  A \times B =
		  |\det
		  \begin{bmatrix}
		  u_11 & v_11 \\
		  u_21 & v_21
		  \end{bmatrix}|
		  \end{equation}
		- #### Inverses
		  To compute the inverse of a matrix, take the *RREF* (Row-Reduced Echelon Form) of the matrix augmented with the identity matrix of identical proportions on the right. The end result of this operation will replace the identity matrix on the right.
		  
		  If there is a row of zeros in the *RREF*, the given matrix is a ((67a25d50-6c70-43fd-bfae-9e0e7ebcd07e)).
		  
		  \begin{equation}
		  A = 
		  \begin{bmatrix}
		  1 & 0 & 2 \\
		  2 & -1 & 3 \\
		  4 & 1 & 8
		  \end{bmatrix}
		  \end{equation}
		  $$\text{so}$$
		  \begin{equation}
		  RREF(
		  \begin{bmatrix}
		  1 & 0 & 2 & 1 & 0 & 0 \\
		  2 & -1 & 3 & 0 & 1 & 0\\
		  4 & 1 & 8 & 0 & 0 & 1
		  \end{bmatrix})
		  =
		  \begin{bmatrix}
		  1 & 0 & 0 & -11 & 2 & 2 \\
		  0 & 1 & 0 & -4 & 0 & 1 \\
		  0 & 0 & 1 & 6 & -1 & -1
		  \end{bmatrix}
		  \end{equation}
		  $$\text{so}$$
		  \begin{equation}
		  A^{-1}=
		  \begin{bmatrix}
		  -11 & 2 & 2 \\
		  -4 & 0 & 1 \\
		  6 & -1 & -1
		  \end{bmatrix}
		  \end{equation}
			- #### Properties
			  If a matrix $A$ is a ((67a25d50-5203-40c8-a7c3-f3e65c7e765d)), then $A\vec{x}=\vec{0}$ has only the solution $\vec{x} = \vec{0}$ - which is called the *trivial solution*.
	-
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
	- ### Transformations
	  Transformations can be thought of as functions, and accordingly, the transformation matrix should always be on the left.
	  
	  Remember that matrix order-of-operations is *right-to-left*.
	  
	  The result of a transformation is often called the *image*, and the set of all possible images is the *range*.
		- ### Common Transformations
			- ### Dilation and Contractions
			  Both take the form $rI_n$.
			  
			  A *dilation* occurs when $r > 1$, and a *contraction* takes place when $1 > r > 0$.
			- ### Rotation
			  A rotation $\theta$ for a matrix in $\mathbb{R}^2$ is the following:
			  
			  **Clockwise**:
			  \begin{bmatrix}
			  \cos{\theta} && \sin{\theta} \\
			  -\sin{\theta} && \cos{\theta}
			  \end{bmatrix}
			  
			  **Counter-Clockwise**:
			  \begin{bmatrix}
			  \cos{\theta} && -\sin{\theta} \\
			  \sin{\theta} && \cos{\theta}
			  \end{bmatrix}
			  
			  There's a helpful formula gathered from this process:
			  $$T(a\vec{u}+b\vec{v}) = aT(\vec{u})+bT(\vec{v})$$
			  $$T((x,y)^T)=xT((1,0)^T)+yT((0,1)^T)$$
			  $$\text{or}$$
			  $$x(\cos{\theta},\sin{\theta})^T=y(-\sin{\theta},\cos{\theta})^T$$
			  $$\text{or}$$
			  \begin{equation}
			  =
			  \begin{bmatrix}
			  \cos\theta & -\sin\theta \\
			  \sin\theta & \cos\theta
			  \end{bmatrix}
			  \begin{bmatrix}
			  x \\ y
			  \end{bmatrix}
			  \end{equation}
				- #### Example
				  Let $T_\theta:\mathbb{R}^2\rarr\mathbb{R}^2$ be rotation by $\theta$. Then,
				  \begin{equation}
				  T_\theta(\vec{u})=
				  \begin{bmatrix}
				  \cos\theta & -\sin\theta \\
				  \sin\theta & \cos\theta
				  \end{bmatrix}
				  =
				  A\vec{u}
				  \end{equation}
			- ### Affine Transformations
			  $$f(\vec{v})=A\vec{v}+\vec{x}$$
			  
			  It's worth noting that this is a common operation in machine learning.
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