# Additional Resources
* [Khan](https://www.khanacademy.org/math/linear-algebra/alternate-bases/change-of-basis/v/lin-alg-transformation-matrix-with-respect-to-a-basis)
- ## Example
  $$L : V_\beta \rarr W_\gamma$$
  $$\text{Basis }V:\text{ (}\beta\text{) }b_1,\ldots,b_n$$
  $$\text{Basis }W:\text{ (}\gamma\text{) }c_1,\ldots,c_n$$
  $$\text{or}$$
  $$[L]_\beta^\gamma$$
  
  We also introduce alternate spaces to:
  $$L:V_{\beta'}\rarr W_{\gamma'}$$
  $$\text{or}$$
  $$[L]_{\beta'}^{\gamma'}$$
  
  $B_{n*n}$ is a matrix from original basis $\beta$ to $\beta'$.
  $C_{m*m}$ is a matrix from original basis $\gamma$ to $\gamma'$.
  
  Our conversion comes out to be:
  $$R_{?}=C^{-1}_{m*m}L_{m*n}B_{n*n}$$
  $$\text{or}$$
  $$R_{m*n}=C^{-1}_{m*m}L_{m*n}B_{n*n}$$
- ## Systematic Approach
	- ### General Problem
	  Can we change the basis so that the matrix:
	  \begin{bmatrix}
	  a & b \\
	  c & d
	  \end{bmatrix}
	  ...becomes easier to use?
	- ### Approaching Via Alternate Basis Vectors
	  \begin{equation}
	  \begin{bmatrix}
	  a & b \\
	  c & d
	  \end{bmatrix}
	  \begin{bmatrix}
	  x \\ y
	  \end{bmatrix}
	  =
	  \lambda
	  \begin{bmatrix}
	  x \\
	  y
	  \end{bmatrix}
	  \end{equation}
	  $$\text{or}$$
	  $$AX = \lambda X$$
	  $$AX=\lambda IX$$
	  $$AX-\lambda IX = \empty_{2*1}$$
	  $$(A-\lambda I)X = \empty_{2*1}$$
	  *Note that* $(A-\lambda I)$ *is by definition a linear map and that* $X$ *and* $\empty_{2*1}$ *are both vectors.*
	  
	  We are guaranteed at least one solution, that being when $X$ is $\empty_{2*1}$. However, we are particularly interested in non-zero values of $X$. Because our linear map $A-\lambda X$ must also have a non-zero determinant to keep it as a one-to-one map, the following is a valid equation:
	  $$\det(A-\lambda I) = 0$$
	  $$\text{or}$$
	  $$\det(\begin{bmatrix}a & b \\ c & d\end{bmatrix} - \begin{bmatrix}\lambda & 0 \\ 0 & \lambda\end{bmatrix}) = 0$$
	  $$\det(\begin{bmatrix}a - \lambda & b \\ c & d - \lambda\end{bmatrix}) = 0$$
	  $$\text{or}$$
	  $$(a-\lambda)(d-\lambda) - (b)(c) = 0$$
	  $$\lambda^2 - (a+d)\lambda + ad - bc = 0$$
	  $$\text{or}$$
	  $$\lambda^2 - \text{trace}(A) + \det(A)=0$$