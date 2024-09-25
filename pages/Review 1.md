### Vector Basis Conversion
To convert a vector V...
\begin{bmatrix} 1 \\ 2 \end{bmatrix} 
...to being described by non-standard basis vectors...
\begin{bmatrix} 1 \\ 1 \end{bmatrix}
...and...
\begin{bmatrix} -1 \\ 1 \end{bmatrix}
..., you must multiply V by the inverse of B, being the inverse of...
\begin{bmatrix} 1 & -1 \\ 1 & 1\end{bmatrix}

You must notate it as:
\begin{equation}
\begin{bmatrix}
\frac{3}{2} \\ \frac{1}{2}
\end{bmatrix}_{B}
\end{equation}
- ### Matrix-Based Equations
	- #### Communicative Law
	  If $A$ is invertible, and $A_{n\cdot n}X_{n\cdot m}=B_{n\cdot m}$, then $\left(A^{-1}\right)\left(AX\right)=A^{-1}B$ and thus $X=A^{-1}B$.
	  
	  Most helpful when $m = 1$.
	- #### Systems in Matrix Notation
	  \begin{cases}
	  x+2y-2z=u\\
	  x+3y-z=v\\
	  y+2z=w
	  \end{cases}
	  
	  Is also representable as:
	  \begin{equation}
	  \begin{bmatrix}
	  1 & 2 & -2 \\
	  1 & 3 & -1 \\
	  0 & 1 & 2
	  \end{bmatrix}
	  \begin{bma}