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
	  
	  To solve this, we can use the Quadratic Formula:
	  $$\lambda = \frac{a+d}{2}\pm\sqrt{(\frac{a+d}{2})^2-(ad-bc)}$$
	  $$\text{or}$$
	  $$=\frac{a+d}{2}\pm\sqrt{(\frac{a-d}{2})^2+bc}$$
	  
	  However, we can immediately note that this only applies in the scenario where $(\frac{a-d}{2})^2 + bc >= 0$ because of the square root.
	- ## Relationship Between the Basis and Characteristic Polynomial
	  $$\det(B^{-1}AB=\lambda I) = 0$$
	  $$\text{or}$$
	  $$\det(B^{-1}AB - \lambda B^{-1}B) = 0$$
	  $$\det(B^{-1}(A-\lambda I)B) = 0$$
	  $$\text{so}$$
	  $$\det(B^{-1})\det(A-\lambda I)\det(B) = 0$$
	  $$\text{or}$$
	  $$\det(A-\lambda I) = 0$$
	  
	  This means that the characteristic polynomial does not care about the basis!
	- ### Example Conversion
	  So, to make our matrix easier to deal with, let's use this process!
	  
	  \begin{bmatrix}
	  0 & 1 \\
	  2 & 3
	  \end{bmatrix}
	  $$\text{or}$$
	  \begin{equation}\det(\begin{bmatrix}
	  0 - \lambda & 1 \\
	  2 & 3 - \lambda
	  \end{bmatrix}) = 0\end{equation}
	  $$\text{so}$$
	  $$\lambda^2-3\lambda-2 = 0$$
	  $$\text{so}$$
	  $$\lambda = \frac{3}{2}\pm\sqrt{\frac{9}{4}+2} = \frac{3 \pm \sqrt{17}}{2}$$
	  
	  Therefore:
	  \begin{equation}
	  \begin{bmatrix}
	  0 & 1 \\
	  2 & 3
	  \end{bmatrix}
	  \begin{bmatrix}
	  x \\ y
	  \end{bmatrix}
	  =
	  \frac{3 \pm \sqrt{17}}{2}
	  \begin{bmatrix}
	  x \\ y
	  \end{bmatrix}
	  \end{equation}
	  $$\text{or}$$
	  \begin{equation}
	  \begin{bmatrix}
	  y \\ 2x + 3y
	  \end{bmatrix}
	  =
	  \frac{3\pm\sqrt{17}}{2}
	  \begin{bmatrix}
	  x \\ y
	  \end{bmatrix}
	  \end{equation}
	  $$\text{so}$$
	  \begin{cases}
	  y = \frac{3\pm\sqrt{17}}{2}x \\
	  2x+3y=\frac{3-\sqrt{17}}{2}y
	  \end{cases}
	  
	  We know one of these cases will be redundant, so we can throw one out. We'll throw out the second one, as it's significantly messier.
	  
	  This creates our two basis:
	  \begin{equation}\begin{bmatrix} 2 \\ 3-\sqrt{17}\end{bmatrix}, \begin{bmatrix}2 \\ 3 + \sqrt{17}\end{bmatrix}\end{equation}
	  
	  Now, we need our $B$!
	  
	  \begin{equation}
	  B = \begin{bmatrix}
	  2 & 2 \\
	  3 - \sqrt{17} & 3 + \sqrt{17}
	  \end{bmatrix}\end{equation}
	  
	  Plugging it into our original equation:
	  $$B^{-1}\begin{bmatrix}0 & 1 \\ 2 & 3\end{bmatrix}B$$
	  $$\text{or}$$
	  $$B^{-1}\begin{bmatrix}0 & 1 \\ 2 & 3\end{bmatrix}\begin{bmatrix}2 & 2 \\ 3 - \sqrt{17} & 3 + \sqrt{17}\end{bmatrix} = B^{-1}\begin{bmatrix}3 - \sqrt{17} & 3+\sqrt{17} \\ 13-3\sqrt{17} & 13 + 3\sqrt{17}\end{bmatrix}$$
	  $$\text{and}$$
	  $$B^{-1}=\frac{1}{4\sqrt{17}}\begin{bmatrix}3+\sqrt{17} & -2 \\ -3 + \sqrt{17} & 2\end{bmatrix}$$
	  $$\text{so}$$
	  $$\frac{1}{4\sqrt{17}}\begin{bmatrix}3+\sqrt{17} & -2 \\ -3 + \sqrt{17} & 2\end{bmatrix}\begin{bmatrix}3 - \sqrt{17} & 3+\sqrt{17} \\ 13-3\sqrt{17} & 13 + 3\sqrt{17}\end{bmatrix}$$