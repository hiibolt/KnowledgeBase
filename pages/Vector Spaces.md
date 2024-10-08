## General Definition
A collection of vectors, where there exists one zero vector. 
Each vector $v$ has a sibling $sv$ (where $s$ is some scalar).
Each vector pair $u,v$ must produce another vector $u+v$.
	- ### Basis Vectors
	  A choice of n vectors $b_1,b_2,\ldots,b_{n}$. It may be that an arbitrary vector $v$ can be written as $v=s_1,b_1+,\cdots,+s_{n}b_{n}$. In which case, vector **spans** the vector space.
	  
	  For example, in $\mathbb{R}^2$, with $\left(1,1\right),\left(1,-1\right),\left(-1,1\right)$:
	  $$\left(x,y\right)=s_1\left(1,1\right)+s_2\left(1,-1\right)+s_3\left(-1,1\right)$$
	  
	  In this case, it becomes immediately apparent that it's not going to work.
	  For example,
	  $$\left(-1,1\right)=a\left(1,1\right)+b\left(1,-1\right)$$
	  $$\text{or}$$
	  $$\left(-1,1\right)=\left(0\right)\left(1,1\right)+\left(-1\right)\left(1,-1\right)$$
	  
	  As a result, we derive that a basis is a collection of vectors that **span** the vector space but has **no redundant vectors**.
	- ### Steps To Verify a Vector Space?
	  All algebraic laws must be satisfied:
	  * $0+v=v$
	  * $v+w=w+v$
	  * $1v=v$
	  * $(u+v)+w=u+(v+w)$
	  * $s(tv) = (st)v$
	  * $s(u+v)=su+sv$
		- ### Example in $\mathbb{R}_{2*2}$:
		  \begin{equation}
		  \begin{bmatrix} 0 & 1 \\ 0 & 0 \end{bmatrix} = x
		  \begin{bmatrix} 1 & 0 \\ 0 & 0 \end{bmatrix} + y
		  \begin{bmatrix} 0 & 0 \\ 1 & 0 \end{bmatrix} + z
		  \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix}
		  \end{equation}
	- ### Characteristics Of A Valid Vector Space
	  The linear map of the constraint *must* be **linear**. For example, a ((66fc4beb-e6bb-4622-ba4c-cb9d1938d5c8)) is **linear**, but a ((66e8828d-8b04-4463-b479-f87150ad4c58)) is not.
- ### Common Spaces
	- #### "$U$" Space
	  $$U=\{u\in M_{2*2} | \text{tr}(u)=0\}$$
	  
	  The common basis vectors are the following three:
	  $$=x\begin{bmatrix}0 & 0\\ 1 & 0\end{bmatrix}+y\begin{bmatrix}0 & 0\\ 1 & 0\end{bmatrix}+z\begin{bmatrix}1 & 0\\ 0 & -1\end{bmatrix}$$
	- #### "$V$" Space
	  $$V=\{v\in M_{2*2}\text{ | }\det(v)=0\}$$
	  
	  **Does it have a zero matrix**:
	  Yes.
	  
	  **We verify that they stay in the space even with scalar multiplication**:
	  $$\det(s\begin{bmatrix}a & b\\ c & d\end{bmatrix})=\det(\begin{bmatrix}sa & sb\\ sc & sd\end{bmatrix})=s^2(ad-bc)$$
	  Yes.
	  
	  **We verify that they stay in the space even with matrix addition**:
	  It does not! There exist examples of matrix addition where two matrices with determinant of zero, when added, do not create a result with a determinant of zero.
	  
	  For example:
	  \begin{equation}
	  \begin{bmatrix}
	  1 & 0 \\
	  0 & 0
	  \end{bmatrix}
	  +
	  \begin{bmatrix}
	  0 & 0 \\
	  0 & 1
	  \end{bmatrix}
	  =
	  \begin{bmatrix}
	  1 & 0 \\
	  0 & 1
	  \end{bmatrix}
	  \end{equation}
	- #### Quadratic Space
	  $$\{a+bx+cx^2\text{ | }\begin{cases}a,b,c\in\mathbb{R}\\ x\in\mathbb{R}\end{cases}\}$$
	  
	  **Does it have a zero matrix**:
	  Yes, $0$.
	  
	  **Does it stay in the space even with scalar multiplication**:
	  Yes.
	  
	  **What are the basis vectors?**
	  $$1,x,x^2$$
- ## ?
  Let's say that we have two vector spaces, $V$ and $W$.
  
  $V$ has the basis $\beta=b_1,\ldots,b_{n}$
  $W$ has the basis $\gamma=c_1,\ldots,c_m$
  
  We have a linear map:
  $$L:V\rightarrow W$$
  $$\left\lbrack L\right\rbrack_{\beta}^{\gamma}$$
  $$\therefore$$
  $$L(b_1)=\alpha_1c_1+\ldots+\alpha_mc_m$$
  
  Our matrix ($M_{m\cdot n}$):
  \begin{equation}
  \begin{bmatrix}
  \alpha_{11} & \ldots & \alpha_{1n} \\
  \ldots & \ldots & \ldots \\
  \alpha_{m1} & \ldots & \alpha_{mn}
  \end{bmatrix}_\beta^\gamma
  \end{equation}