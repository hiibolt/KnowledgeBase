## Transformations
Transformations can be thought of as functions, and accordingly, the transformation matrix should always be on the left.

Remember that matrix order-of-operations is *right-to-left*.

The result of a transformation is often called the *image*, and the set of all possible images is the *range*.
- ## Common Transformations
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