## Scalar Multiplication
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
- ## Addition
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
- ## Transpose
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
- ## Vector Length
  Denoted by $$||\vec{v}||$$.
  
  For example, in $$\mathbb{R}^2$$:
  $$||\vec{v}|| = \sqrt{a^2 + b^2}$$
  
  In $$\mathbb{R}^3$$:
  $$||\vec{v}|| = \sqrt{a^2 + b^2 + c^2}$$
  
  In $$\mathbb{R}^n$$:
  $$||\vec{v}|| = \sqrt{a_1^2 + a_2^2 + ... + a_n^2}$$
- ## Dot Product
  id:: 6787f568-1935-41ae-a8f4-adcc0fe55c86
  $$(a_1,...,a_n)^{(T)}\cdot (b_1,...,b_n)^{(T)}=a_1b_1+...+a_nb_n$$
  $$\vec{x}\cdot\vec{y} = ||\vec{x}||||\vec{y}||\cos{\theta}$$
	- ### Cauchy-Schwarz
	  Guarantees that for any $\vec{x},\vec{y}\in\mathbb{R}^n$,
	  $$-1<\frac{\vec{x}\cdot\vec{y}}{||\vec{x}||||\vec{y}||}<1$$
	- ### Implications
	  Firstly, we must recall the ((67893c87-26ba-4786-9c07-c8155c2f7015)).
	  
	  By knowing this, we can use the dot product to find perpendicular vectors by solving.
	  
	  In general, this formula is represented for a $$\mathbb{R}^2$$ vector $$\vec{x}={a,b}$$, you should select a vector $$\vec{s} = {\pm b,\pm a}$$ where *one of* $a$ or $b$ is negative.
	  
	  The length of a vector squared is the same vector dot itself, giving the following:
		- #### Hypotenuse Theorem
		  $${||\vec{x}||}^2=\vec{x}\cdot\vec{x}$$
	- ### Special Properties
	  $$\vec{u}\cdot(\vec{v}+\vec{w})=a_1(b_1+c_1)+...+a_n(b_n+c_n)$$
	  $$\text{or}$$
	  $$=\vec{u}\cdot\vec{v}+\vec{u}\cdot\vec{w}$$
- ## Projection
  $$P_{\vec{v}}{\vec{u}}=\frac{\vec{u}\cdot\vec{v}}{\vec{v}\cdot\vec{v}}\vec{v}$$
  
  $P_{\vec{v}}\vec{u}$ is read as "projecting $\vec{u}$ onto $\vec{v}$.
- ## Null Space
  For a given matrix $A$, the *null space* or *kernel*  is the solution set of $A\vec{x}=\vec{0}$
  
  Represented as:
  $$\text{Null}(A), \text{Nul}(A), \text{Ker}(A)$$
  
  A kernel is also:
  $$f:S\rarr T$$
  ...where some element of $T$ plays the "role" of the number $0$. In other words, the identity for some operation $T$.
  
  In this setting:
  $$\text{Ker}(f)=\{\vec{x}\in S : f(\vec{x}) = 0\}$$
  $$f(\vec{x})=A\vec{x}$$
- ## Matrix Multiplication
  The general process is to go *down* the rows of the first (left) matrix and *across* the columns of the second (right) matrix, and take the ((6787f568-1935-41ae-a8f4-adcc0fe55c86)) of the two.
	- ### Algebraic Properties (of addition, technically)
	  Let $A$, $B$, and $C$ be $mxn$ matrices. Then,
	  $$A+B = B + A$$
	  $$A+(B+C)=(A+B)+C$$
	  $$\text{There exists a unique matrix }0_{mn}\text{ such that } A+0_{mn}=A$$
	  ...where $0_{mn}$ is a ((67912a9e-2bd7-4de0-ae70-fea77995ff98)).
	  $$A+(-A)=0$$
	  $$-A=(-1)*A$$
	- ### Properties
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
	- ### Using Sigma Notation
	  $$c_{ij}=\sum_{\lambda=1}^n(a_{i\lambda}b_{i\lambda})$$
- ## Determinant
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
	- ### 2x2
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
	- ### 3x3 
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
	- ### 4x4
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
- ## Cross Product
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
- ## Inverses
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
	- ### Properties
	  If a matrix $A$ is a ((67a25d50-5203-40c8-a7c3-f3e65c7e765d)), then $A\vec{x}=\vec{0}$ has only the solution $\vec{x} = \vec{0}$ - which is called the *trivial solution*.
- ## Imaging
  The *image* of a matrix is the set:
  $$\{A\vec{x}:\vec{x}\in \mathbb{R}^n\}\subseteq \mathbb{R}^m$$
  $$\text{...where }A\in M_{m,n}$$
  ...although it's difficult to picture this.
  
  In other words:
  \begin{equation}
  A_{m x n}*
  \begin{pmatrix}
  x_1 \\ \dots \\ x_n
  \end{pmatrix}_{n x 1}
  =
  \begin{pmatrix}
  y_1 \\ \dots \\ y_m
  \end{pmatrix}_{m x 1}
  \end{equation}
  
  This is notated as:
  $$\text{Image(A)}\text{ or }\text{Im}(A)$$
  $$\text{Im}(f):\{f(\vec{x}):\vec{x}\in S\}\subseteq T$$