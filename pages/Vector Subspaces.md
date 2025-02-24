## Definition
Let $V$ be a *vector space* and $\empty \ne W \subseteq V$. If $W$ is a vector space with respect to the operations in $V$, then $W$ is called a *subspace* of $V$. Every vector space has two subspaces $\{\vec{0}\}$ and $V$ itself.
- ## Determining Vector Space Validity
  **Theorem**: Let $V$ be a vector space with operations $\oplus$ and $\odot$. Let $W$ be a non-empty subset of $V$. Then $W$ is a subspace if and only if:
  * $W$ is closed under $\oplus$
  * $W$ is closed under $\odot$
	- ### Example
	  The subset of $\mathbb{R^3}$ given by:
	  \begin{equation}
	  \{
	  \begin{pmatrix}
	  a \\ b \\ a - b 
	  \end{pmatrix}
	  : a,b \in \mathbb{R}
	  \}
	  \end{equation}
	  ...is a subspace of $\mathbb{R^3}$.
	  
	  Verifying $\odot$:
	  \begin{equation}
	  \alpha
	  \begin{pmatrix}
	  a \\ b \\ a - b 
	  \end{pmatrix}
	  =
	  \begin{pmatrix}
	  \alpha a \\ \alpha b \\ \alpha a - \alpha b 
	  \end{pmatrix}
	  \in
	  S
	  \end{equation}
	  
	  Verifying $\oplus$:
	  \begin{equation}
	  \begin{pmatrix}
	  a \\ b \\ a - b 
	  \end{pmatrix}
	  +
	  \begin{pmatrix}
	  c \\ d \\ c - d 
	  \end{pmatrix}
	  =
	  \begin{pmatrix}
	  a + c \\ b + d \\ a + c - b - d 
	  \end{pmatrix}
	  \in
	  S
	  \end{equation}
	  $$\therefore S\text{ is a valid subspace.}$$
- ## Common Subspaces
	- ### $P_2$ (polynomials of degree $\le 2$)
	  This is a subspace of $P_3$!
	  
	  Or, generally, $P_n$ is a subspace of $P_{n+1}$.